# Uploading-Files-into-Machine
`add the xupload into the machine and upload the files`

> one line:
```
echo "<!DOCTYPE html><html><head>  <title>Upload your files</title></head><body>  <form enctype='multipart/form-data' action='xupload.php' method='POST'>    <p>Upload your file</p>    <input type='file' name='uploaded_file'></input><br />    <input type='submit' value='Upload'></input>  </form></body></html><?PHP  if(!empty(\$_FILES['uploaded_file']))  {    \$path = '/tmp/';    \$path = \$path . basename( \$_FILES['uploaded_file']['name']);    if(move_uploaded_file(\$_FILES['uploaded_file']['tmp_name'], \$path)) {      echo 'The file '.  basename( \$_FILES['uploaded_file']['name']).       ' has been uploaded';    } else{        echo 'There was an error uploading the file, please try again!';    }  }?>" > xupload.php
```
![image](https://ibb.co/txQtgKN)
