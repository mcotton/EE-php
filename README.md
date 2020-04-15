## Introduction ##

PHP example for the [Eagle Eye Networks API](https://apidocs.eagleeyenetworks.com).  The wrapper is in `een.php`.

### Docker ###

Check-out `docker-compse.yaml` for details.

Run it with `docker-compose up --build -d`


### Getting Started ###

    //create a new instance of the API
    $een = new EagleEyeNetworks();


    //supply your EEN credentials in `config.php`
    $username = '<username>';
    $password = '<password>';


    //pass your username/password into the login function and get your user object
    $user_obj = $een->login($username, $password);


    //now that you're logged-in you can get all your devices
    $user_devices = $een->list_devices();


    //you can use page.html and jquery.preview.js to show previews on your site
    $('#preview').cameraPreview({ 'camera_id': '1001abcd' });

