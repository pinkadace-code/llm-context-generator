# LLM Context Generator

Rīks kas automātiski ģenerē MySQL datubāzes kontekstu un izmanto AI lai atbildētu uz jautājumiem par datiem.

## Kas tas dara?

1. Pieslēdzas MySQL serverim un iegūst datubāzes struktūru
2. Izveido kontekstu (aprakstu) par datiem
3. Izmanto Groq AI lai ģenerētu SQL vaicājumus no dabiskās valodas
4. Izpilda SQL un iegūst datus
5. Apraksta rezultātus latviešu valodā ar AI

## Nepieciešamās bibliotēkas

pip install mysql-connector-python groq pandas

## Konfigurācija

Izveido `.env` failu (vai Colab Secrets) ar šādiem mainīgajiem:
- `GROQ_API_KEY` — Groq API atslēga no console.groq.com

## Lietošana

Atver `llm_context_generator.ipynb` Google Colab un palaid šūnas secībā.

## Datubāzes struktūra

Sistēma strādā ar `direct_payments` datubāzi:
- `organisations` — organizācijas un to nozares
- `mandates` — tiešmaksājumu pilnvaras
- `payments` — maksājumi
