
Questo documento stabilisce il protocollo tecnico per la 
generazione di prompt e scene Noir, basato sulle direttive di Google Cloud 
(Reliability & Grounding). Il sistema NotebookLM deve utilizzare queste regole 
come "Source of Truth" per ogni Artifact generato.

Ecco le regole pratiche estratte dalle sezioni "Prompt Engineering" e "RAG" del documento Google Cloud per strutturare un prompt complesso, seguite dal template operativo per una scena Noir.

1. **System Prompting**: Fornisci istruzioni prima di qualsiasi input per stabilire lo **stile** (es. linee guida cinematografiche), il **tono** e il formato della risposta.

2. **Integrazione del Contesto (Grounding)**: Inserisci dettagli specifici e "fondati" per evitare risposte generiche. Questo include requisiti tecnici, dettagli ambientali e preferenze di stile.

3. **Approccio Telescopico**: Inizia con un prompt generico, valuta i risultati, identifica i gap di performance e crea prompt progressivamente più specifici.

4. **Few-shot Prompting**: Inserisci almeno **cinque esempi** di coppie input-output nel prompt per guidare il modello verso la creatività e l'accuratezza desiderate.

5. **Chain-of-thought (CoT)**: Chiedi esplicitamente al modello di **spiegare il suo ragionamento** o di seguire passaggi logici prima di generare l'output finale, migliorando così la coesione narrativa.

6. **Riduzione del Rumore**: Se il modello produce risultati irrilevanti, riduci il numero di informazioni o esempi forniti per aumentare la rilevanza di quelli rimanenti.

--------------------------------------------------------------------------------

Template Operativo: Scena Noir per AI Video

Questo template utilizza il **Few-shot** per mostrare lo stile e la **Chain-of-thought** per guidare la logica visiva.

**[ISTRUZIONI DI SISTEMA]** Agisci come un esperto direttore della fotografia specializzato in Noir classico. Il tuo obiettivo è generare descrizioni visive ad alto contrasto (chiaroscuro) con atmosfere cupe e ricche di tensione.

**[FEW-SHOT EXAMPLES]**

• **Input**: Un uomo aspetta sotto un lampione.

• **Output**: Inquadratura dal basso. Luce giallastra taglia la nebbia densa. L'ombra dell'uomo si allunga bizzarramente sul pavé bagnato. Bianco e nero granuloso.

• **Input**: Una donna entra in un ufficio fumoso.

• **Output**: Controluce attraverso le veneziane. Strisce di luce e ombra tagliano il volto della donna. Il fumo della sigaretta danza in volute lente sopra una scrivania di mogano.

**[CHAIN-OF-THOUGHT REASONING]** Prima di scrivere la descrizione finale per la nuova scena, esegui questi passaggi:

1. **Analizza il conflitto**: Qual è la tensione emotiva della scena?

2. **Definisci la luce**: Come possono le ombre nascondere o rivelare le intenzioni dei personaggi?

3. **Dettaglia la consistenza**: Descrivi elementi come pioggia, fumo o riflessi per dare profondità.

4. **Scegli l'inquadratura**: Determina l'angolo di ripresa che enfatizza il mood noir.

**[INPUT SCENA NOIR]** **Descrivi la seguente scena:** [Inserisci qui la tua idea, es: "Un detective trova una prova compromettente in un vicolo cieco"]

--------------------------------------------------------------------------------
