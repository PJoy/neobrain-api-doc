# QUESTION FORMS ADMIN SIDE
## VERSION 2

Au chargement du questionnaire, nouvelle variable sérialisée : dataAssessment

_Routes AJAX :_

- __{{ path('company.assessmentquestion.new') }}__ > return JsonResponse(['creation' => boolean ])
- __{{ path('company.assessmentquestion.edit', { 'assessmentQuestion': id à renseigner }) }}__ > return JsonResponse(['edition' => boolean ])
- __{{ path('company.assessmentquestion.delete', { 'assessmentQuestion': id à renseigner }) }}__ > return JsonResponse(['delete' => boolean ])

_types de questions_
### Type : Message (_message_)

```json
{   
    "id": null, 
    "assessment_id": 5,  
    "type": "message",  
    "label": "votre message",
    "position": 1
}
```

### Type : Simple (_simple_)

```json
{
    "id": null, 
    "assessment_id": 5,    
    "type": "simple",
    "label": "Intitulé de la question",
    "position": 1,
    "description": "ma description"
}
```

### Type : Question ouverte (_justify_)

```json
{
    "id": null, 
    "assessment_id": 5,    
    "type": "justify",
    "label": "Intitulé de la question",
    "position": 1,
    "description": "ma description"
}
```

### Type : Sélection (_select_)

```json
{
    "id": null,    
    "assessment_id": 5,
    "type": "select",
    "label": "Intitulé de la question",
    "position": 1,
    "description": "ma description",
    "options": {
        "choices" : [
            "Intitulé de l'option 1",
            "Intitulé de l'option 2",
            "Intitulé de l'option 3"
        ]
    }
}
```

### Type : Choix (_choice_)

```json
{
    "id": null, 
    "assessment_id": 5,    
    "type": "choice",
    "label": "Intitulé de la question",
    "position": 1,
    "description": "ma description",
    "max_choices": 3,
    "options": {
        "choices" : [
            "Intitulé de l'option 1",
            "Intitulé de l'option 2",
            "Intitulé de l'option 3"
        ]
    }
}
```

### Type : Notation (_range_)

```json
{
    "id": null, 
    "assessment_id": 5,    
    "type": "range",
    "label": "Intitulé de la question",
    "position": 1,
    "description": "ma description",
    "options": {
        "labels": {
            "left":  "Label à gauche (facultatif)",
            "center":  "Label au milieu (facultatif)",
            "right":  "Label à droite (facultatif)"
        },
        "display": "heart",
        "min": 1,
        "max": 5
    }
}
```

### Type : Evaluation des objectifs (_eval-obj_)

```json
{
    "todo": "TODO"
}
```

### Type : Proposition d'objectifs (_eval-prop_)

```json
{
    "todo": "TODO"
}
```

### Type : Tableau (_array_)

```json
{
    "todo": "TODO"
}
```

### Type : Complétion du profil (_profile_)

```json
{
    "todo": "TODO"
}
```

### Type : Compétences (_skills_)

```json
{
    "todo": "TODO"
}
```

## VERSION 1 (formData)
### Type : Message (message)

```
#parameters: array:5 [
    "assessment_id" => "5"
    "type" => "message"
    "label" => "Votre message"
    "questionId" => ""
    "position" => "1"
  ]
```

### Type : Simple (simple)

```
#parameters: array:6 [
    "assessment_id" => "5"
    "type" => "simple"
    "label" => "Intitulé de la question"
    "questionId" => ""
    "position" => "1"
    "options" => "{"label_simple_commentaire":"Intitulé du commentaire (facultatif)"}"
  ]
```

### Type : Question ouverte (justify)

```
#parameters: array:5 [
    "assessment_id" => "5"
    "type" => "justify"
    "label" => "Intitulé de la question"
    "questionId" => ""
    "position" => "1"
  ]
```

### Type : Sélection (select)

```
#parameters: array:8 [
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

### Type : Choix (choice)

```
#parameters: array:9 [
    "assessment_id" => "5"
    "type" => "choice"
    "label" => "Intitulé de la question"
    "questionId" => ""
    "position" => "1"
    "options_type" => "choice_option"
    "answer_count" => "3"
    "options" => "Intitul%C3%A9%20de%20l'option%201,Intitul%C3%A9%20de%20l'option%202%20,Intitul%C3%A9%20de%20l'option%203%20"
    "optionscommentaire" => "{"label_choice_commentaire":"Intitulé du commentaire (facultatif)"}"
  ]
```

### Type : Notation (range)

```
#parameters: array:6 [
    "assessment_id" => "5"
    "type" => "range"
    "label" => "Intitulé de la question"
    "questionId" => ""
    "position" => "1"
    "options" => "{"range_type":"heart","indicator_type":"","range_end":5,"range_start":1,"label_range_commentaire":"Intitulé du commentaire (facultatif)","label_center":"Label au centre (facultatif)","label_right":"Label à droite (facultatif)","label_left":"Label à gauche (facultatif)"}"
  ]
```
