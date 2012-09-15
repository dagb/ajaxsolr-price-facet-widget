ajaxsolr-price-facet-widget
===========================

AjaxSolr Facet Widget for presenting price ranges

Add the following to render facet links

	AjaxSolr.theme.prototype.pricegroup = function (value, label,handler) {
     return $('<a href="#" />').append(value).append( '(' + label + ')<br/>').click(handler);
	};

To add the widget to your page

	Manager.addWidget(new AjaxSolr.PriceGroupWidget({
			id: 'salesPrice',
         target: '#salesPrice',
			field: 'salesPrice',
         fields: ['salesPrice']
		}));


Add the following parameters, with suitable values

			  'f.salesPrice.facet.limit': -1,
			  'f.salesPrice.facet.range.start': 1000.0,
			  'f.salesPrice.facet.range.end': 9999999,
			  'f.salesPrice.facet.range.gap': 50000.0,
	
