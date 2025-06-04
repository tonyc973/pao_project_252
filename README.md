# Definirea Sistemului Bancar Java

Acest proiect reprezintă un **sistem bancar simplificat** dezvoltat în Java. Prin intermediul unei interfețe CLI, utilizatorul poate crea conturi, efectua tranzacții, programa plăți și adăuga notițe, toate acțiunile fiind logate într-un sistem de audit, respectiv într-o bază de date. 

---

## Funcționalități principale 

1. **Creare cont economii sau curent**  
   - Permite înregistrarea unui cont nou, cu detalii precum ID, titular, sold inițial, dobândă sau comision.

2. **Depunere bani într-un cont existent**  
   - Introduce suma dorită în soldul unui cont specific.

3. **Retragere bani dintr-un cont**  
   - Retrage o sumă specificată din soldul unui cont existent.

4. **Afișare tranzacții pentru un cont**  
   - Afișează istoricul tranzacțiilor unui cont dat.

5. **Afișare toate conturile**  
   - Listează toate conturile înregistrate în sistem.

6. **Ștergere cont**  
   - Elimină un cont bancar identificat prin ID.

7. **Creare plată programată**  
   - Permite setarea unei plăți recurente sau programate cu dată, sumă și destinatar.

8. **Afișare plăți programate**  
   - Afișează lista tuturor plăților programate în sistem.

9. **Adăugare notiță la cont**  
   - Permite salvarea unei notițe textuale asociată unui cont (titlu, conținut, dată).

10. **Afișare notițe**  
    - Listează toate notițele salvate în sistem.

---

## Tipuri de obiecte din aplicatie

| Obiect            | Descriere                                                                 |
|-------------------|---------------------------------------------------------------------------|
| `ContBancar`      | Clasă de bază pentru conturile bancare, cu atribute comune (ID, sold etc.) |
| `ContCurent`      | Subclasă a `ContBancar` care are comision la tranzacții                    |
| `ContEconomii`    | Subclasă a `ContBancar` care beneficiază de dobândă anuală                 |
| `Tranzactie`      | Reprezintă o depunere sau retragere asociată unui cont                     |
| `PlataProgramata` | Reprezintă o plată viitoare, cu detalii despre sumă, dată și destinatar    |
| `Notita`          | Obiect cu titlu, conținut și dată asociat unui cont                        |
| `ServiciuBancarDAO` | Componenta principală ce gestionează toate operațiunile bancare           |
| `AuditService`    | Singleton care loghează toate acțiunile efectuate în sistem                |



