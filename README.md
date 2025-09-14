# Stripe API Postman Collection

Ova kolekcija sadrži primjere zahtjeva za testiranje **Stripe API-ja** u sandbox okruženju.  
Možete koristiti kolekciju da vježbate plaćanje, refundiranje i testiranje idempotency logike.

## 🚀 Setup

### 1. Import kolekcije
1. Preuzmite fajl **`STRIPE_API.json`**.
2. U Postmanu kliknite **Import** → izaberite fajl.
3. Kolekcija će se pojaviti pod nazivom **STRIPE API**.

### 2. Import environment-a
1. Preuzmite fajl **`Stripe_API_Environment.postman_environment.json`**.
2. U Postmanu kliknite **Import** → izaberite fajl.
3. U gornjem desnom uglu Postmana izaberite **Stripe API Environment**.
4. Otvorite environment i zamijenite vrijednost varijable:
   - `STRIPE_SECRET_KEY` → unesite svoj test secret key sa [Stripe Dashboard-a](https://dashboard.stripe.com/test/apikeys).

### 3. Pokretanje requesta
- ✅ `KreirajPlacanjeSuccessful` → treba vratiti **200**
- ❌ `KreirajPlacanjeUnsuccessful` → primjer greške (400)
- 💸 `RefundirajPlacanje` → refundira uspješno plaćanje
- 🔒 `Neautorizovan zahtjev` → testira 401 Unauthorized
- ♻️ `PlacanjeSaIdempotencyKeySuccessful` / `Unsuccessful` → testira idempotency ponašanje

## 🔑 Napomena

- **Nikada ne objavljujte svoj stvarni secret key** (`sk_live_...`) u javnim repozitorijima.  
- Ova kolekcija koristi placeholder `{{STRIPE_SECRET_KEY}}` → korisnici moraju sami unijeti svoj ključ.  
