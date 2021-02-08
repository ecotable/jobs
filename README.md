# Test technique Écotable

## Instructions

À partir d'une liste de fournisseurs (`data/providers.json`) et d'une liste de factures et de leurs éléments (`data/invoices.json`), générer une liste contenant les informations suivantes :

- Une liste de tous les éléments contenus dans les factures, avec les informations suivantes :
  - description de l'élément
  - quantité
  - numéro de la facture
  - ID du fournisseur si l'on peut le faire correspondre aux fournisseurs que l'on connait déjà
  - l'élément est-il bio? (organic) basé sur sa description ou si l'on sait que le fournisseur ne fait que des produits bios
- Une liste de tous les fournisseurs inconnus dans les factures

Par exemple, en se basant sur les données présentes dans `data/providers.json` et `data/invoices.json` :

```json
{
  "items": [
    {
      "description": "gigot entier",
      "quantity": 3,
      "invoice_number": "FR1234",
      "provider_id": 1,
      "organic": true,
    },
    {
      "description": "Biscuit dessert AB",
      "quantity": 100,
      "invoice_number": "IV9876",
      "provider_id": 4,
      "organic": true,
    }
    #, ...
  ],
  "unknown_providers": ["Pierre Paul Jacques"]
}
```

## Précisions
- Votre programme doit être appelable de la manière suivante : `ruby ecotable.rb providers.json invoices.json`
- Considerez que les données des factures proviennent d'un outil automatisé de lecture (OCR), il peut y avoir des imprécisions de lecture.
- Si un fournisseur a la propriété `"organic": true`, on sait que 100% de ses produits seront BIO.
- Pour déterminer si un produit est BIO en fonction de sa description, vous avez champs libre.


## Capacités attendues :
- Autonomie
- Attention au détail
- Proactivité
- Force de proposition
