---
layout: normal
title: EA Shop Navigation
name: ea-shop-navigation
description: EA Shop Navigation
category: navigation
---

## EA Shop Navigation

<div class="example-title">HTML / Liquid</div>
{% raw %}
```liquid
{% assign MainHierarchy = Hierarchy["SHOP-NAVIGATION"] %}
{% if MainHierarchy %}
<nav data-component="ea-shop-navigation" class="ea-shop-navigation show-for-large">
    <ul class="ea-shop-navigation__menu">
    {% for node in MainHierarchy.HierarchyNodes %}
        {% if node.HierarchyNodes %}
            <li class="ea-shop-navigation__level ea-shop-navigation__level--one {{ node.HierarchyLevel.Code }}">
                <a href="{{ node.NavigateUrl | Downcase }}">{{ node.HierarchyLevel.Description }}</a>
                <div class="ea-shop-navigation__dropdown">
                    {% for panel in node.HierarchyNodes %}
                        <div class="ea-shop-navigation__panel {{ panel.HierarchyPanel.Description | Upcase | Replace: ' ','-' }}">
                        <span class="ea-shop-navigation__panel-title">{{ panel.HierarchyPanel.Title }}</span>
                          <ul>            
                              {% for child in panel.HierarchyNodes %}    
                                  {% if child.DirectLink %}
                                      <li class="ea-shop-navigation__level ea-shop-navigation__level--two"><a href="{{ child.NavigateUrl | Downcase }}">{{ child.DirectLink.Description }}</a></li>                  
                                  {% endif %}
                                  {% if child.HierarchyLevel %}
                                      <li class="ea-shop-navigation__level ea-shop-navigation__level--two"><a href="{{ child.NavigateUrl | Downcase }}">{{ child.HierarchyLevel.Description }}</a></li>  
                                  {% endif %}
                                  {% if child.ContentManagedPage %}
                                      <li class="ea-shop-navigation__level ea-shop-navigation__level--two"><a href="{{ child.NavigateUrl | Downcase }}">{{ child.ContentManagedPage.Description }}</a></li> 
                                  {% endif %}  
                                  {% if child.ContentManagedRegion %}
                                     <li class="ea-shop-navigation__level ea-shop-navigation__level--two">{{ ContentManagedRegion[child.ContentManagedRegion.Code].Contents }}</li>
                                  {% endif %} 
                               {%endfor%}
                           </ul>                    
                       </div>
                    {%endfor%}
                </div>
            </li>
        {% else %}
            {% if node.DirectLink %}
                <li class="ea-shop-navigation__level ea-shop-navigation__level--one {{ node.HierarchyLevel.Code }}">
                    <a href="{{ node.NavigateUrl | Downcase }}">{{ node.DirectLink.Description }}</a>
                </li>                   
            {% endif %}
            {% if node.HierarchyLevel %}
                <li class="ea-shop-navigation__level ea-shop-navigation__level--one {{ node.HierarchyLevel.Code }}">
                    <a href="{{ node.NavigateUrl | Downcase }}">{{ node.HierarchyLevel.Description }}</a>
                </li>
            {% endif %}
            {% if node.ContentManagedPage %}
                <li class="ea-shop-navigation__level ea-shop-navigation__level--one {{ node.HierarchyLevel.Code }}">
                    <a href="{{ node.NavigateUrl | Downcase }}">{{ node.ContentManagedPage.Description }}</a>
                </li>
            {% endif %}
        {% endif %}
    {% endfor %}
    </ul>
</nav>
{% endif %}
```
{% endraw %}

<div class="example-title">SCSS</div>
{% raw %}
```scss
.ea-shop-navigation{
	background: $primary-color;

	// Navigation menu container
	&__menu{
		@extend .menu;
		width:1200px;
		margin:0 auto;
		display: flex;
		flex-direction: row;
		position: relative;  
	}	

	// Navigation levels
	&__level{
		
		// Level one
		&--one{
			flex-grow: 1;
			text-align: center;

			> a{
				color:$white;
				position: relative;
				transition: .25s;
				text-transform: uppercase;

				&:hover{
					background: scale-color($primary-color, $lightness: 10%);
				}
			}

			// Level one hover
			&:hover{
				a{
					&:after{
						content:"";
						display:inline-block;
						bottom:0;
						position:absolute;
						margin-left:-5px;
						width:0;
						left:50%;
						height:0;
						border-left:5px solid transparent;
						border-right:5px solid transparent;
						border-bottom:5px solid $white;
					}
				}
				.ea-shop-navigation__dropdown{
					display: flex;
				}
			}
		}

		// Level two
		&--two{
			> a{
			}

			&:hover{
				a{
					color: $secondary-color;
				}
			}
		}

		// Specific level styling
		&.SALE{
			>a{
				background: $secondary-color;

				&:hover{
					background: scale-color($secondary-color, $lightness: 10%);
				}
			}

		}
	}

	// Navigation submenu dropdown
	&__dropdown{
		flex-direction: row;
    	position: absolute;
	    top: 100%;
	    width: 100%;
	    background: $white;
        //border: 1px solid $border-color;
    	border-top: 0;
	    z-index: 1;
	    left:0;

	    // Initially set to display none
		display: none;
	}

	// Navigation dropdown panels
	&__panel{
		flex-grow: 1;
		padding: 2rem;
		text-align: left;

		ul{
			@extend .menu;
			@extend .vertical;
			
			li{
				a{
					padding:.5rem 0;
				}
			}
		}
	}

	&__panel-title{
		display: block;
		font-weight: bold;
		margin: 0 0 .5rem;
	}

}
```
{% endraw %}