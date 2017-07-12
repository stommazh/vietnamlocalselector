# Vietnam local selector - JavaScript plugin

*Create HTML Select element for Vietnam province, district and ward.*

## Basic usage

First, create 3 HTML Select elements for province, district and ward with name 'ls_province', 'ls_district' and 'ls_ward' respectively:

```html
<select name="ls_province"></select>
<select name="ls_district"></select>
<select name="ls_ward"></select>
```
Finally, include the plugin to your document,create instance of the plugin and pass the identify of selectors to an object as parameter:
```html
<script src="vietnamlocalselector.js"></script>
<script>
	var localpicker = new LocalPicker({
		province: "ls_province",
		district: "ls_district",
		ward: "ls_ward"
    	});
</script>
```
## Options

```javascript
  var options = {
  	    /*
            HTML Selector. You can pass value of name, id or class. 
            It will automatically detect exist elements for you.
            Example: 'myIdOrClass','#myId', '.myClass', 'myName'
            */
            province: 'ls_province',	
            district: 'ls_district',	
            ward: 'ls_ward',			
                      
            /*
            Define value for option tag. Valid option: id|name           
            */
            getValueBy: 'id',           
            
            //Placeholder text
            provinceText: 'Chọn tỉnh / thành phố',
            districtText: 'Chọn quận / huyện',
            districtNoText: 'Địa phương này không có quận / huyện',
            wardText: 'Chọn phường / xã',
            wardNoText: 'Địa phương này không có phường / xã',
            
            // Default value if no location exist
            emptyValue: " ",
            
            // Hide option where no local exist
            hideEmptyValueOption: true,
            
            // Hide place-holder option (first option)
            hidePlaceHolderOption: true,
            
            /*
            Include local level on option text as prefix
            Example: true = Quận Bình Thạnh | false = Bình Thạnh
            */
            provincePrefix: false,
            districtPrefix: true,
            wardPrefix: true,
            
            /*
            Include local level in option tag's attribute
            */
            levelAsAttribute: true,
            levelAttributeName: "data-level",
  };
```
