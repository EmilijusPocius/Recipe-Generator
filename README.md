
***

# Maisto receptų generatorius

TNLP kurso namų darbas. Programa sugeneruoja receptą ir patiekalo nuotrauką pagal įvestus ingredientus, naudojant **Custom Transformer** modelį + **Gemini** (teksto redagavimui) + **Stable Diffusion** (vaizdui).

## Kaip paleisti (Google Colab)

Kodas pritaikytas veikti **Google Colab** aplinkoje su GPU, su CPU taip pat veikia, tik vaizdo generavimas labai lėtas.

### 1. Nustatymai
1. Atidarykite `TNLP_RecipeGenerator.ipynb` failą per Google Colab.
2. Pasirinkite meniu: **Runtime** -> **Change runtime type**.
3. Nustatykite **Hardware accelerator** į **T4 GPU**.

### 2. API Rakto įvedimas
Reikalingas raktas teksto redagavimui (Gemini):
1. Kairėje meniu juostoje spauskite **rakto ikoną** (Secrets).
2. Spauskite **Add new secret**.
   * **Name:** `GOOGLE_API_KEY`
   * **Value:** Jūsų Google AI Studio raktas.
3. Įjunkite **Notebook access** varnelę.

### 3. Paleidimas
1. Spauskite **Runtime** -> **Run all**.
2. Palaukite, kol susiinstaliuos, užsikraus bibliotekos ir modeliai.
3. **Nuslinkite į failo apačią** – ten rasite UI ingredientų įvedimui.
4. Ingredientus veskite atskirtus tarpais, pvz.: "eggs minced beef salt peeled tomatoes"

## Reikalavimai

Pagrindinės bibliotekos (įdiegiamos automatiškai notebook'e):
*   `tensorflow`
*   `pandas`
*   `numpy`
*   `google-generativeai`
*   `diffusers`, `transformers`
*   `ipywidgets`
