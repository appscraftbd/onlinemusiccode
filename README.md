# onlinemusiccode

এইভাবে কোড লিখেন ।<br>
সবার উপরে public class এর মধ্যে এই variable ধরবেন ।<br>
কোডঃ<br>
private MediaPlayer mediaPlayer;<br>
-------------------------------<br>
button এর onClick এর মধ্যে এই কোড লিখবেন ।<br>
কোডঃ<br>
String url = "এখানে mp3 এর url দিন ";<br>
mediaPlayer = new MediaPlayer();<br>
mediaPlayer.setAudioStreamType(AudioManager.STREAM_MUSIC);<br>
try {<br>
mediaPlayer.setDataSource(url);<br>
mediaPlayer.prepareAsync();<br>
mediaPlayer.setOnPreparedListener(new MediaPlayer.OnPreparedListener() {<br>
@Override<br>
public void onPrepared(MediaPlayer mp) {<br>
mediaPlayer.start();<br>
}<br>
});<br>
} catch (IOException e) {<br>
e.printStackTrace();<br>
}<br>
