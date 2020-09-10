# increment-and-decrement-buttons-for-input-field


HTML START:


 <div class="form-group">
                                    <div class="control-label col-md-4  col-sm-4 col-xs-5"><b>QTY :</b></div>
                                    <div class="col-md-8 col-sm-8 col-xs-7">
                                        <div class="container">
                                            <input type="button" onclick="decrementValue(<?php echo $i ?>)" value="-" />
                                            <input type="text" name="quantity[]" value="0" maxlength="2" max="10" min="0" size="1" style="align:center" id="number<?php echo $i ?>" />
                                            <input type="button" onclick="incrementValue(<?php echo $i ?>)" value="+" />
                                        </div>
                                    </div>
                                </div>
                                
   HTML END:
   SCRIPT START:
   
   
   <script type="text/javascript">
    function incrementValue(val)
    {
//    alert("hi");exit;
        var value = parseInt(document.getElementById('number' + val).value, 10);
//    alert(value);exit;
        value = isNaN(value) ? 0 : value;
        if (value < 10) {
            value++;
            document.getElementById('number' + val).value = value;
        }
    }
    function decrementValue(val)
    {
        var value = parseInt(document.getElementById('number' + val).value, 10);
        value = isNaN(value) ? 0 : value;
        if (value > 1) {
            value--;
            document.getElementById('number' + val).value = value;
        }

    }
</script>


 SCRIPT END:
