### window.open()함수를 사용하지 않고 자식창을 만들어 팝업효과를 내는 방법

<script type="text/javascript">
    function fn_layerInit_evalExel(){
            $('#mask').show();
            $('#layerInit_evalExel').show().css("margin-top", "10px");
    }
<script>

<div class="layer type01" id="layerInit_evalExel" style="width: 420px; margin-left: 55px; margin-top: -20px; display: none;">
	<h3 class="tit">자식 팝업</h3>

	<div class="btnLayerClose"><a href="javascript:void(0);" class="closeLayer" id="layerInitClose" onclick="javascript:fn_layerInitClose();"><img src="./images/popup/btn_layer_close02.gif" alt=""></a></div>
	<div class="inner" style="padding:20px 37px;">
       	<div id="evalExel" class="txt_c">
	    <br><a href="javascript:void(0);" class="btn_gray" style="width:150px;" onclick="fn_download('down1'); return false;" >다운로드 1</a>
	       	<a href="javascript:void(0);" class="btn_gray" style="width:150px;" onclick="fn_download('down2'); return false;" >다운로드 2</a>
       	</div>
	</div>
</div>
<!-- 팝업열릴 시 부모창 어둡게-->
<div id="mask" style="display: none;"></div>