+---------------------------------+-----------------------------------+
| **Navn** | **Passerer fra lav side** |
+=================================+===================================+
| **Mål** | Lade et skib anvende |
| | slusesystemet til at bevæge sig |
| | fra den lave side af |
| | slusesystemet til den høje side |
+---------------------------------+-----------------------------------+
| **Initiering** | Et skib holder indenfor |
| | kamerafeltet "kamera lav" |
+---------------------------------+-----------------------------------+
| **Aktører** | Skibet |
+---------------------------------+-----------------------------------+
| **Antal samtidige forekomster** | 1 (Der er kun én mulig forekomst |
| | af gangen) |
+---------------------------------+-----------------------------------+
| **Prækonditioner** | Slusen er operationel, ikke i |
| | brug, og der er vand til skibene |
+---------------------------------+-----------------------------------+
| **Postkonditioner** | Skibet befinder sig på den høje |
| | side og har passeret kamerafeltet |
| | "kamera høj" |
+---------------------------------+-----------------------------------+
| **Hovedscenarie** | 1. Et skib holder indenfor |
| | kamerafeltet "kamera lav" |
| | |
| | 2. Slusen begynder at dræne\ |
| | _ **EXT1**: Et skib holder |
| | indenfor kamerafeltet "kamera |
| | høj"_ |
| | |
| | 3. Indtil den når lav vandstand, |
| | som detekteret af "kamera |
| | midt" |
| | |
| | 4. Sluseport lav åbner |
| | |
| | 5. Skibet sejler ind i |
| | sluseelevatoren |
| | |
| | 6. Når den forlader kamerafelt |
| | "kamera lav" og bevæger sig |
| | ind i kamerafelt "kamera |
| | midt" |
| | |
| | 7. Sluseport lav lukker |
| | |
| | 8. Sluseelevatoren fyldes med |
| | vand |
| | |
| | 9. Indtil den når vandstand høj, |
| | som detekteret af "kamera |
| | midt" |
| | |
| | 10. Sluseport høj åbner |
| | |
| | 11. Skibet sejler ud af |
| | kamerafelt "kamera midt", ind |
| | i kamerafelt "kamera høj" |
| | |
| | 12. Skibet forlader kamerafelt |
| | "kamera høj" |
| | |
| | 13. Sluseport høj lukker.\ |
| | _ **EXT2**: Der er et andet |
| | skib i kamerafelt "kamera |
| | høj"_ |
| | |
| | 14. Sluseelevator drænes indtil |
| | den når et midtpunkt, som |
| | detekteret af "kamera midt", |
| | og afventer det næste input |
| | fra kamerafelterne. |
+---------------------------------+-----------------------------------+
| | **EXT1**: Et skib holder |
| | indenfor kamerafeltet "kamera |
| | høj"_ |
| | |
| | 1. Vent til **passerer høj |
| | side** er afsluttet. |
| | |
| | 2. Forsæt use case. |
| | |
| | **EXT2**: Der er et andet |
| | skib i kamerafelt "kamera |
| | høj"_ |
| | |
| | 1. Afslut use case. |
| | |
| | 2. Forsæt use case **passerer |
| | høj side.** |
+---------------------------------+-----------------------------------+








+---------------------------------+-----------------------------------+
| **Navn**                        | **Passerer fra lav side**         |
+=================================+===================================+
| **Mål**                         | Lade et skib anvende              |
|                                 | slusesystemet til at bevæge sig   |
|                                 | fra den lave side af              |
|                                 | slusesystemet til den høje side   |
+---------------------------------+-----------------------------------+
| **Initiering**                  | Et skib holder indenfor           |
|                                 | kamerafeltet "kamera lav"         |
+---------------------------------+-----------------------------------+
| **Aktører**                     | Skibet                            |
+---------------------------------+-----------------------------------+
| **Antal samtidige forekomster** | 1 (Der er kun én mulig forekomst  |
|                                 | af gangen)                        |
+---------------------------------+-----------------------------------+
| **Prækonditioner**              | Slusen er operationel, ikke i     |
|                                 | brug, og der er vand til skibene  |
+---------------------------------+-----------------------------------+
| **Postkonditioner**             | Skibet befinder sig på den høje   |
|                                 | side og har passeret kamerafeltet |
|                                 | "kamera høj"                      |
+---------------------------------+-----------------------------------+
| **Hovedscenarie**               | 1.  Et skib holder indenfor       |
|                                 |     kamerafeltet "kamera lav"     |
|                                 |                                   |
|                                 | 2.  Slusen begynder at dræne\     |
|                                 |     * **EXT1**: Et skib holder   |
|                                 |     indenfor kamerafeltet "kamera |
|                                 |     høj"*                         |
|                                 |                                   |
|                                 | 3.  Indtil den når lav vandstand, |
|                                 |     som detekteret af "kamera     |
|                                 |     midt"                         |
|                                 |                                   |
|                                 | 4.  Sluseport lav åbner           |
|                                 |                                   |
|                                 | 5.  Skibet sejler ind i           |
|                                 |     sluseelevatoren               |
|                                 |                                   |
|                                 | 6.  Når den forlader kamerafelt   |
|                                 |     "kamera lav" og bevæger sig   |
|                                 |     ind i kamerafelt "kamera      |
|                                 |     midt"                         |
|                                 |                                   |
|                                 | 7.  Sluseport lav lukker          |
|                                 |                                   |
|                                 | 8.  Sluseelevatoren fyldes med    |
|                                 |     vand                          |
|                                 |                                   |
|                                 | 9.  Indtil den når vandstand høj, |
|                                 |     som detekteret af "kamera     |
|                                 |     midt"                         |
|                                 |                                   |
|                                 | 10. Sluseport høj åbner           |
|                                 |                                   |
|                                 | 11. Skibet sejler ud af           |
|                                 |     kamerafelt "kamera midt", ind |
|                                 |     i kamerafelt "kamera høj"     |
|                                 |                                   |
|                                 | 12. Skibet forlader kamerafelt    |
|                                 |     "kamera høj"                  |
|                                 |                                   |
|                                 | 13. Sluseport høj lukker.\        |
|                                 |     * **EXT2**: Der er et andet  |
|                                 |     skib i kamerafelt "kamera     |
|                                 |     høj"*                         |
|                                 |                                   |
|                                 | 14. Sluseelevator drænes indtil   |
|                                 |     den når et midtpunkt, som     |
|                                 |     detekteret af "kamera midt",  |
|                                 |     og afventer det næste input   |
|                                 |     fra kamerafelterne.           |
+---------------------------------+-----------------------------------+
|                                 |     * **EXT1**: Et skib holder    |
|                                 |     indenfor kamerafeltet "kamera |
|                                 |     høj"*                         |
|                                 |                                   |
|                                 | 1.  Vent til **passerer høj       |
|                                 |     side** er afsluttet.          |
|                                 |                                   |
|                                 | 2.  Forsæt use case.              |
|                                 |                                   |
|                                 | **EXT2:** Skibet prioriterer at   |
|                                 | et skib er ved nuværende          |
|                                 | vandhøjde.                        |
|                                 |                                   |
|                                 | 1.  Afslut use case.              |
|                                 |                                   |
|                                 | 2.  Forsæt use case **passerer    |
|                                 |     høj side.**                   |
+---------------------------------+-----------------------------------+
