# zadanie4

## Postać obiektów JSON

UWAGA! Nowo wysyłane obiekty nie mają parametru 'id'!

### Film
Obiekt wysyłany lub aktualizowany nie ma parametrów 'id', 'rating' oraz 'comments'

    {
    "id" : 1,
    "name" : "Godfather",
    "polishName" : "Ojciec chrzestny",
    "worldPremiere" : "2016-01-01",
    "polishPremiere" : "2016-02-03",
    "director" : "Adam Mialczynski",
    "writer" : "Jonasz Goldsztajn",
    "producer" : "Mili Entr.",
    "rating" : 3.5,
    "comments" : [
      {
        "id" : 1,
        "nick" : "Jan",
        "content" : "biedota!"
      }
    ]
    }

Przykładowy obiekt do testów:

    {
    "name" : "Godfather",
    "polishName" : "Ojciec chrzestny",
    "worldPremiere" : "2016-01-01",
    "polishPremiere" : "2016-02-03",
    "director" : "Adam Mialczynski",
    "writer" : "Jonasz Goldsztajn",
    "producer" : "Mili Entr."
    }

    
### Aktor

    {
     "id" : 1,
     "name" : "Cezary",
     "surname" : "Pazura"
    }

### Komentarz
    {
     "nick" : "Jan Kowalski",
     "content" : "Opinia"
    }

### Ocena

    {
     "id" : 1,
     "value" : 5
    }
    
## Adresy URL i metody HTTP

### Filmy
Wszystkie filmy

    GET /movies
    
Jeden film z określonym ID

    GET /movies/{id}
    
Lista aktorów grających w filmie z określonym ID

    GET /movies/{id}/actors
    
Utworzenie nowego filmu - należy wysłać prawidłowy obiekt JSON

    POST /movies
    
Aktualizacja filmu o określonym ID - należy wysłać prawidłowy obiekt JSON

    PUT /movies/{id}

### Komentarze i oceny

Komentarze do filmu o określonym ID

    GET /movies/{id}/comments
    
Wysłanie nowego komentarza - należy przesłać prawidłowy obiekt JSON

    POST /movies/{id}/comments
    
Usunięcie komentarza o ID1 do filmu z ID2

    DELETE /movies/{id2}/comments/{id1}
    
Wystawienie oceny do filmu - należy przesłać prawidłowy obiekt JSON

    POST /movies/{id}/rating
    
### Aktorzy

Lista wszystkich aktorów

    GET /actors
    
Jeden aktor o podanym ID

    GET /actors/{id}
    
Dodanie nowego aktora - należy wysłać prawidłowy obiekt JSON

    POST /actors
    
Wyświetlenie wszystkich filmów w których grał aktor

    GET /actors/{id}/movies
    
Przydzielenie aktora ID1 do filmu ID2

    PUT /actors/{id1}/movies/{id2}
