# How-to-calculate-data-birthday-age-at-watson-assistant-for-an-answer-

I suffered to get this solution, it seems stupid, but I think it is worth sharing, it was not easy to do it alone.
I hope that if anyone needs this, they will find this sharing more quickly, and not have to fry the brains like me.

Json example

```json
{
  "output": {
    "generic": [
      {
        "values": [
          {
            "text": "print $age "
          }
        ],
        "response_type": "text",
        "selection_policy": "sequential"
      }
    ]
  },
  "context": {
    "age": "<? ( T(Integer).parseInt(today().split('-').get(0)) - ( new Date(2007,06,06).year ) ) ?>"
  }
}
```
