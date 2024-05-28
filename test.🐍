from PIL import Image, ImageDraw, ImageFont

def split_sentence(sentence):
    words = sentence.split()
    result = []
    current_sentence = ''
    for word in words:
        if len(current_sentence) + len(word) + 1 < 13:
            current_sentence += ' ' + word if current_sentence else word
        else:
            result.append(current_sentence.strip())
            current_sentence = word
    if current_sentence:
        result.append(current_sentence.strip())
    return result

def draw1(splitted_sentences):
    im = Image.open("template.png")
    draw = ImageDraw.Draw(im)
    font_type = ImageFont.truetype("Poppins Medium.ttf", 150)
    x = 105
    y = 218
    for i in splitted_sentences:
        draw.text((x,y), text= i, fill=(255,255,255), font=font_type)
        y+=190
    if len(splitted_sentences)<=3:
        im.show()
    else:
        pass


sentence = input()
draw1(split_sentence(sentence))

