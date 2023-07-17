# onlinemusiccode
এইভাবে কোড লিখেন ।
সবার উপরে public class এর মধ্যে এই variable ধরবেন ।
কোডঃ
private MediaPlayer mediaPlayer;
-------------------------------
button এর onClick এর মধ্যে এই কোড লিখবেন ।
কোডঃ
String url = "এখানে mp3 এর url দিন ";
mediaPlayer = new MediaPlayer();
mediaPlayer.setAudioStreamType(AudioManager.STREAM_MUSIC);
try {
mediaPlayer.setDataSource(url);
mediaPlayer.prepareAsync();
mediaPlayer.setOnPreparedListener(new MediaPlayer.OnPreparedListener() {
@Override
public void onPrepared(MediaPlayer mp) {
mediaPlayer.start();
}
});
} catch (IOException e) {
e.printStackTrace();
}
