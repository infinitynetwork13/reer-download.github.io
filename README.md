## Reel Downloader

- Instagram
- Threads

  ### Instagram

  * import
```JAVA
import com.infinity.network13.instagram.Instagram;
import com.infinity.network13.Ultra;
```
* Request
```JAVA
String url = "https://www.instagram.com/reel/C7B5g3rKV7tV/?igsh=MXI4NWJ6bnIyeWszbw==";
String return_data = Instagram.request(url);
JSONObject data = new JSONObject(return_data);
if (data.has("type")){
  Boolean type = data.getBoolean("type");
  if(type){
    if(data.has("username")){
      String username = data.getString("username");
    }
    if(data.has("icon")){
      String icon = data.getString("icon");
    }
    if (data.has("video")){
      String video = data.getString("video");
    }
  } else {
    String massage = data.getString("massage");
  }
}
```
