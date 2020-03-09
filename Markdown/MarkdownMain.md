---
pdf_document:
  toc: true
geometry: margin=2cm
---

\pagebreak

## Opgave 1 - Aktør/kontekstdiagrammer.

Herunder følger aktør/kontekstdiagrammer og dertilhørend beskrivelser.

![Actor Context diagram](../UCD/ActorContext.png)

Beskrivelse af aktører:

| Aktør     | Type  | Beskrivelse                                                                                                   |
| --------- | ----- | ------------------------------------------------------------------------------------------------------------- |
| Skib      | Prim. | Skibet bruger systemet. Skibet sejler frem til slusesystemet for at passere fra høj til lav eller vice versa. |
| Kaptajn   | Prim. | Kaptajnen sejler skibet og bruger dermed slusesystemet for at komme frem til sin destination.                 |
| Kamera    | Sek.  | Kamera registrerer indkomne skibe på høj og lav side. Kamera holder øje med vandstanden i slusekammeret.      |
| Sluseport | Sek.  | Sluseportene åbner og lukker efter systemets behov for at skibe kan passere.                                  |

\pagebreak

## Opgave 2 - Use cases

Herunder ses usecase diagrammet for slusesystemet

![Use case diagram](../UCD/UseCases.png)

\pagebreak

## Opgave 3 - Fully Dressed use case

Herunder ses et Fully dressed use case diagram for slusesystemet.

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
|                                 | **EXT1**: Et skib holder          |
|                                 |     indenfor kamerafeltet "kamera |
|                                 |     høj"                           |
|                                 |                                   |
|                                 | 1.  Vent til **passerer høj       |
|                                 |     side** er afsluttet.          |
|                                 |                                   |
|                                 | 2.  Forsæt use case.              |
|                                 |                                   |
|                                 | **EXT2**: Der er et andet         |
|                                 |     skib i kamerafelt "kamera     |
|                                 |     høj"                          |
|                                 |                                   |
|                                 | 1.  Afslut use case.              |
|                                 |                                   |
|                                 | 2.  Forsæt use case **passerer    |
|                                 |     høj side.**                   |
+---------------------------------+-----------------------------------+

\pagebreak

## Opgave 4 - FURPS+ // MoSCoW

Herunder er de ikke funktionelle-krav opstillet efter (F)URPS+ modellen.

- **U**sability
  - Ét skib ind **skal** ind, ét skib **skal** ud.
  - Der **bør** være en indikation om hvorvidt portkammeret er ledigt.
  - Der **kunne** være mulighed for, at se om der skibe på den modstatte side.
- **R**eliability
  - Systemet **skal** kunne startes op på 72 timer.
  - Ved nedtid **bør** systemet kunne startes igen på 24 timer.
  - Nedetid **bør** være < 5% ved 2mnd. brug baseret på flg. reliability udregning;
    - $24\text{h} \cdot 2\text{m} = 1440\text{h}$.
    - $\frac{72\text{h}}{1440\text{h}}=5\%$
  - Portkammeret **bør** drænes på 2 timer - muligøre service / rengøring.
- **P**erformance
  - Et skib **bør** kunne passerer slusesystmet på **30** minutter.
  - Et skib **skal** kunne passerer på 90 minutter.
  - Kun ét skib ad gangen **skal kunne** passere.
  - Kaptajn el. lign **kunne** signalere nødstop.
- **S**upportability
  - Kameraene **kunne** serviceres hvert 3. år for bedste effekt.

## Opgave 5 - Accepttest

Herunder ses accepttest af slusesystemet.

| **Use case under test** | **Passerer fra lav side**                   |     |     |     |
| ----------------------- | ------------------------------------------- | --- | --- | --- |
| **Scenarie**            | Hovedscenarie                               |     |     |     |
| **Prækondition**        | Sluseporten er operationel og klar til brug |     |     |     |

| **Step** | **Handling**                                                           | **Forventet observation/resultat**                                                                       | **Faktisk observation/resultat** | **OK/FAIL** |
| -------- | ---------------------------------------------------------------------- | -------------------------------------------------------------------------------------------------------- | -------------------------------- | ----------- |
| **1**    | Sejl skibet frem til sluseporten fra lav side                          | Kamera på lav side opfanger skibet og sluseporten begynder at dræne vand fra slusen                      |                                  |             |
| **2**    | Vent på dræning af vand i slusen                                       | Vandet i slusen drænes indtil vandstanden er samme som på lav side                                       |                                  |             |
| **3**    | Vent på at sluseporten på lav side åbner                               | Sluseporten på lav side begynder at åbne når vandstanden er ens i slusen og på lav side                  |                                  |             |
| **4**    | Sejl skibet ind i slusen                                               | Kamera i slusen opfanger at skibet er inde i slusen og porten på lav side lukker                         |                                  |             |
| **5**    | Vent på at sluseporten på lav side lukker og vandet hæves til høj side | Når sluseporten er lukket drænes vand ind fra høj side indtil vandstanden er ens i slusen og på høj side |                                  |             |
| **6**    | Vent på at sluseporten på høj side åbner                               | Sluseporten på høj side begynder at åbne når vandstanden er ens i slusen og på høj side                  |                                  |             |
| **7**    | Sejl skibet ud af sluseporten og ud af kamerafeltet på høj side        | Sluseporten på høj side lukkes og vandet drænes til neutral position                                     |                                  |             |

\pagebreak


| **Use case under test** | **Passerer fra høj side**                   |     |     |     |
| ----------------------- | ------------------------------------------- | --- | --- | --- |
| **Scenarie**            | Hovedscenarie                               |     |     |     |
| **Prækondition**        | Sluseporten er operationel og klar til brug |     |     |     |

| **Step** | **Handling**                                                            | **Forventet observation/resultat**                                                        | **Faktisk observation/resultat** | **OK/FAIL** |
| -------- | ----------------------------------------------------------------------- | ----------------------------------------------------------------------------------------- | -------------------------------- | ----------- |
| **1**    | Sejl skibet frem til sluseporten fra høj side                           | Kamera på høj side opfanger skibet og sluseporten begynder at fylde vand i slusen         |                                  |             |
| **2**    | Vent på at vandet i slusen hæves                                        | Slusen fyldes med vand indtil vandstanden matcher høj side                                |                                  |             |
| **3**    | Vent på at sluseporten på høj side åbner                                | Sluseporten på høj side begynder at åbne når vandstanden i slusen matcher høj side        |                                  |             |
| **4**    | Sejl skibet ind i slusen                                                | Kamera i slusen opfanger at skibet er inde i slusen og porten på høj side lukker          |                                  |             |
| **5**    | Vent på at sluseporten på høj side lukker og vandet sænkes til lav side | Når sluseporten er lukket sænkes vandstanden i slusen indtil vandstanden matcher lav side |                                  |             |
| **6**    | Vent på at sluseporten på lav side åbner                                | Sluseporten på lav side begynder at åbne når vandstanden i slusen matcher lav side        |                                  |             |
| **7**    | Sejl skibet ud af sluseporten og ud af kamerafeltet på lav side         | Sluseporten på lav side lukkes og vandet hæves til neutral position                       |                                  |             |

\pagebreak

| **Use case under test** | **Passerer fra lav side**                                     |     |     |     |
| ----------------------- | ------------------------------------------------------------- | --- | --- | --- |
| **Scenarie**            | Extension: Samtidig ankomst af skibe ved både lav og høj side |     |     |     |
| **Prækondition**        | Sluseporten er operationel og klar til brug                   |     |     |     |

| **Step** | **Handling**                                                          | **Forventet observation/resultat**                                                            | **Faktisk observation/resultat** | **OK/FAIL** |
| -------- | --------------------------------------------------------------------- | --------------------------------------------------------------------------------------------- | -------------------------------- | ----------- |
| **1**    | Sejl et skib frem til både sluseport på høj side og lav side samtidig | Kamera på både høj og lav side opfanger et skib i deres kamerafelt                            |                                  |             |
| **2**    | Vent på systemet                                                      | Systemet skal påbegynde use case _Passerer fra høj side_                                      |                                  |             |
| **3**    | Vent på gennemgang af use case _Passerer fra høj side_                | Systemet skal påbegynde use case _Passerer fra lav side_ når skibet fra høj side har passeret |                                  |             |
|          |                                                                       |                                                                                               |                                  |             |
