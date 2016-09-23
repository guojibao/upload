# upload
iframe-uoload
//ajax upload
//表单绑定submit event 
form.on('submit',function(){
    //here code ajax do something
    //checked formdate
    if(window.FormData){
        var formData = new FormData();
        //make one upload from value upload file
        formData.append('upload',document.getElementById('upload').files[0]);
        var xhr = new XMLHttpRequest();
        xhr.open('POST',$(this).attr('action'));
        
        //complate callback
         xhr.onload = function (){
            if (xhr.status === 200){
            console.log('done');
         } else {
            console.log('error');
         }
    };
    xhr.send(formData);
}
