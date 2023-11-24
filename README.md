# Urdu_Text_to_Speech_with_gtts
It contains a simple Python script using the gtts library to convert Urdu text to speech. The script generates an audio file and plays it, providing a basic example of text-to-speech functionality in Urdu.
Coding:-
from gtts import gTTSimport pygameimport ostext_urdu = "Your Urdu text goes here"tts_urdu = gTTS(text_urdu, lang='ur')tts_urdu.save("output_urdu.mp3")def play_mp3(mp3_file):    pygame.mixer.init()      pygame.mixer.music.load(mp3_file)     pygame.mixer.music.play()  if __name__ == "__main__":    mp3_file = "output_urdu.mp3"      play_mp3(mp3_file)    input("Press Enter to quit...")    pygame.mixer.music.stop()    pygame.quit()    file_path = "output_urdu.mp3"        try:        os.remove(file_path)    except Exception as e:        pass
