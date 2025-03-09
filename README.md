import random

# Film ve karakter/olay eşleştirmelerini tanımla
matches = {
    "Inception": ["Rüyalar", "Leonardo DiCaprio", "Katmanlar"],
    "The Lord of the Rings": ["Yüzük", "Ork", "Hobbit"],
    "Pulp Fiction": ["Valiz", "John Travolta", "Umar Thurman"],
    "Interstellar": ["Uzay", "Zaman", "Kara delik"],
    "The Shawshank Redemption": ["Hapishane", "Kaçış", "Tim Robbins"],
    "Fight Club": ["Dövüş", "Sabun", "Brad Pitt"],
    "The Silence of the Lambs": ["Hannibal", "Ajan", "Yamyam"],
    "Hababam Sınıfı": ["Mahmut Hoca", "İnek Şaban", "Okul"],
}

def main():
    print("Zorlaştırılmış Film Karakteri veya Olay Eşleştirme Oyunu'na Hoş Geldiniz!")
    film, hints = random.choice(list(matches.items()))
    
    print(f"İpucu: {', '.join(hints)}")
    guess = input("Bu hangi film? ").strip()
    
    if guess.lower() == film.lower():
        print("Tebrikler! Doğru tahmin.")
    else:
        print(f"Maalesef, yanlış tahmin. Doğru cevap: {film}")

if __name__ == "__main__":
    main()
