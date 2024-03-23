<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>Drag and Drop</title>
<link rel="stylesheet" href="https://code.jquery.com/ui/1.12.1/themes/base/jquery-ui.css">
<style>
    #sourceDiv, #targetDiv {
        width: 200px;
        min-height: 200px;
        border: 1px solid black;
        margin: 20px auto;
        overflow: auto; /* Mobil cihazlarda kaydırma desteği için ekledik */
    }
    .draggableItem {
        width: 50px;
        height: 50px;
        background-color: blue;
        margin: 10px;
        cursor: move;
        text-align: center;
        line-height: 50px;
        transition: background-color 0.3s ease;
    }
    .draggableItem.ui-draggable-dragging {
        background-color: lightgray; /* Sürükleme sırasında rengi değiştir */
    }
    #targetDiv span {
        display: inline-block;
        width: 100%;
        margin: 5px 0;
        border: 1px solid #ccc;
        padding: 5px;
        box-sizing: border-box;
    }
    .draggableItem.ui-draggable-disabled {
        opacity: 0.5; /* Pasif hale geldiğinde opaklık ayarla */
        cursor: move; /* Mobil cihazlarda da sürükleme özelliğini etkinleştir */
    }
    .undoButton {
        display: none; /* Başlangıçta geri alma butonlarını gizle */
    }
	.target.hover {
		background-color: #ccffcc; /* Çok açık yeşil */
	}
	.target.filled {
		background-color: #d9f5d9; /* Daha koyu yeşil */
	}
</style>
</head>
<body>

<div id="sourceDiv">
    <div class="draggableItem" id="1">Item 1</div>
    <div class="draggableItem" id="2">Item 2</div>
    <div class="draggableItem" id="3">Item 3</div>
</div>

<div id="targetDiv">
    <span class="target" id="input1"><span class="area" ></span><button class="undoButton" data-id="" style="display:none">Geri Al</button></span>
    <span class="target" id="input2"><span class="area" ></span><button class="undoButton" data-id="" style="display:none">Geri Al</button></span>
    <span class="target" id="input3"><span class="area" ></span><button class="undoButton" data-id="" style="display:none">Geri Al</button></span>
</div>

<script src="https://code.jquery.com/jquery-3.6.3.min.js"></script>
<script src="https://code.jquery.com/ui/1.12.1/jquery-ui.js"></script>
<script>
$(document).ready(function() {
	init();
	
    var prevDropTargets = {}; // Önceki bırakma hedeflerini saklamak için nesne
    
    // Sürükleyici işlemi başlat
    $(".draggableItem").draggable({
        revert: function(valid) {
            // Eğer öğe geçerli bir bırakma hedefine düşmediyse geri al
            return !valid || !valid.target;
        },
        helper: "clone" // Sürüklenen öğenin bir kopyasını oluştur
    });
    
    // Bırakma işlemi için hedef alanı belirle
    $(".target").droppable({
		over: function(event, ui) {
			$(this).addClass("hover"); // Hedef alanın üzerine gelindiğinde stil ekleyin
		},
		out: function(event, ui) {
			$(this).removeClass("hover"); // Hedef alanın dışına çıkıldığında stil kaldırın
		},
        drop: function(event, ui) {
			$(this).removeClass("hover");
			
			// Hedef alanı dolu hale getirin ve stil ekleyin
			$(this).addClass("filled");
		
            // Sürüklenen elemanın değerini al
            var value = ui.draggable.text();
			
            // Bırakma hedefini sakla
            var targetId = $(this).attr("id");
			
			// daha önce değer varsa
			if($("#"+targetId + " > .area").text()!="") {
				var dataId = $("#"+targetId + " > .undoButton").attr("data-id");
				$("#"+targetId + " > .area").text("");
				$("#sourceDiv > #" + dataId).draggable("enable");
				$("#"+targetId + " > .undoButton").attr("data-id", "");
				$("#"+targetId + " > .undoButton").hide();
			}
			
			
			// Sadece bırakılan span alanına değeri yerleştir
			$("#"+targetId + " > .area").text(value);
		
			// Sürüklenen elemanı pasif hale getir
			ui.draggable.draggable("disable");
		
			prevDropTargets[targetId] = this;
			$("#"+targetId + " > .undoButton").show();
			$("#"+targetId + " > .undoButton").attr("data-id", ui.draggable.attr("id"));
			
        }
    });
   
    // Geri alma butonu işlevselliği
    $(".undoButton").click(function() {
        var targetId = $(this).attr("data-id");
        var parent = $(this).parent().attr("id");
        // var prevDropTarget = prevDropTargets[targetId];
        if (targetId) {
            // Hedef alanını temizle ve sürüklenen elemanı aktifleştir
            // $(prevDropTarget).empty();
            // prevDropTargets[targetId] = null;
			$("#"+parent + " > .area").text("");
			$("#sourceDiv > #" + targetId).draggable("enable");
			$(this).attr("data-id", "");
			$(this).hide();
			
			// Hedef alanı boş hale getirin ve stil kaldırın
			$("#" + parent).removeClass("filled");
        }
    });
});
function touchHandler(event) {
    var touch = event.changedTouches[0];

    var simulatedEvent = document.createEvent("MouseEvent");
        simulatedEvent.initMouseEvent({
        touchstart: "mousedown",
        touchmove: "mousemove",
        touchend: "mouseup"
    }[event.type], true, true, window, 1,
        touch.screenX, touch.screenY,
        touch.clientX, touch.clientY, false,
        false, false, false, 0, null);

    touch.target.dispatchEvent(simulatedEvent);
    // event.preventDefault();
}

function init() {
    document.addEventListener("touchstart", touchHandler, true);
    document.addEventListener("touchmove", touchHandler, true);
    document.addEventListener("touchend", touchHandler, true);
    document.addEventListener("touchcancel", touchHandler, true);
}
</script>

</body>
</html>
