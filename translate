require "google/cloud/translate"

project_id = "project_id_goes_here"
key_file_path = "place_keypath_here"

translate = Google::Cloud::Translate.new(project_id: project_id, credentials: key_file_path)

def translate_text(text, source_language, target_language, translate)
  translation = translate.translate(text, from: source_language, to: target_language)
  translation.text
end

puts "Enter the text you want to translate:"
text_to_translate = gets.chomp

source_languages = ["bg", "hr", "cs", "da", "nl", "et", "fi", "fr", "de", "el", "hu", "ga", "it", "lv", "lt", "mt", "pl", "pt", "ro", "sk", "sl", "es", "sv", "en", "he", "ru", "ja", "ko"]
target_languages = ["bg", "hr", "cs", "da", "nl", "et", "fi", "fr", "de", "el", "hu", "ga", "it", "lv", "lt", "mt", "pl", "pt", "ro", "sk", "sl", "es", "sv", "en", "he", "ru", "ja", "ko"]

source_languages.each do |source_language|
  target_languages.each do |target_language|
    translated_text = translate_text(text_to_translate, source_language, target_language, translate)
    puts "Source Language: #{source_language}, Target Language: #{target_language}"
    puts "Original Text: #{text_to_translate}"
    puts "Translated Text: #{translated_text}"
    puts "------------"
  end
end
