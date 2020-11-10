# Type : Message

```#parameters: array:5 [
    "assessment_id" => "5"
    "type" => "message"
    "label" => "Votre message"
    "questionId" => ""
    "position" => "1"
  ]
```

# Type : Simple

```#parameters: array:6 [
    "assessment_id" => "5"
    "type" => "simple"
    "label" => "Intitulé de la question"
    "questionId" => ""
    "position" => "1"
    "options" => "{"label_simple_commentaire":"Intitulé du commentaire (facultatif)"}"
  ]
```

# Type : Question ouverte

```#parameters: array:5 [
    "assessment_id" => "5"
    "type" => "justify"
    "label" => "Intitulé de la question"
    "questionId" => ""
    "position" => "1"
  ]
```

# Type : Sélection

```#parameters: array:8 [
    "assessment_id" => "5"
    "type" => "select"
    "label" => "Intitulé de la question"
    "questionId" => ""
    "position" => "1"
    "options_type" => "select_option"
    "options" => "Intitul%C3%A9%20de%20l'option%201,Intitul%C3%A9%20de%20l'option%202,Intitul%C3%A9%20de%20l'option%203"
    "optionscommentaire" => "{"label_select_commentaire":"Intitulé du commentaire (facultatif)"}"
  ]
```

# Type : Choix

```#parameters: array:9 [
    "assessment_id" => "5"
    "type" => "choice"
    "label" => "Intitulé de la question"
    "questionId" => ""
    "position" => "1"
    "options_type" => "choice_option"
    "answer_count" => "5"
    "options" => "Intitul%C3%A9%20de%20l'option%201,Intitul%C3%A9%20de%20l'option%202%20,Intitul%C3%A9%20de%20l'option%203%20"
    "optionscommentaire" => "{"label_choice_commentaire":"Intitulé du commentaire (facultatif)"}"
  ]
```

# Type : Notation

```#parameters: array:6 [
    "assessment_id" => "5"
    "type" => "range"
    "label" => "Intitulé de la question"
    "questionId" => ""
    "position" => "1"
    "options" => "{"range_type":"heart","indicator_type":"","range_end":5,"range_start":1,"label_range_commentaire":"Intitulé du commentaire (facultatif)","label_center":"Label au centre (facultatif)","label_right":"Label à droite (facultatif)","label_left":"Label à gauche (facultatif)"}"
  ]
```
