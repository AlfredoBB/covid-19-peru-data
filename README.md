**Última actualización**: 2020-04-28 21:09:33 UTC

Motivación
----------

MINSA está publicando en su cuenta de Twitter y en la sección de
“Noticias” del portal del gobierno peruano, comunicados con información
sobre COVID-19, pero no hay un repositorio de datos abiertos que pueda
ser usado por todos.

Seguiré actualizando diariamente mientras esta información se encuentre
disponible.

Espero que pronto MINSA ponga un repositorio de datos abiertos con la
información nececasaria, y cuando eso ocurra, este repositorio ya no se
actualzará.

Importante
----------

**2020-03-03**: A partir de hoy, MINSA ha puesto una “Sala situacional”
oficial en
<a href="https://covid19.minsa.gob.pe/sala_situacional.asp" class="uri">https://covid19.minsa.gob.pe/sala_situacional.asp</a>.
Los datos de este día fueron tomados de las “Sala Situacional” del
MINSA, el cual no tiene información (al día de hoy) acerca del número de
recuperados

**2020-04-08**: A partir de hoy, en la “Sala situacional” se comenzaron
a publicar el número de casos confirmados por pruebas moleculares (PCR),
y por “pruebas rápidas” (serológicas) por cada región. Esto se ha
agregado a los datos.

**2020-04-12**: A partir de este día, la “Sala Situacional” ha dejado de
publicar el número de fallecimientos por región, y ha agregado el número
de casos positivos confirmados por ambos tipos de pruebas: moleculares
(PCR) y serológica (“rapida”).

**2020-04-13**: La “Sala Situacional” no fue actualizada en este día
(revisado a las 21:53h), por lo que no hay datos disponibles de pruebas
por región.

**2020-04-14**: La “Sala Situacional” está mostrando nuevamente los
fallecimientos y los resultados de pruebas positivas por región.

**2020-04-15**: La “Sala Situacional” ya no publica los casos en que se
confirmaron por ambos tipos de pruebas, para las regiones.

**2020-04-23**: Se ha ampliado la cuarentena hasta el 2020-05-10.
Cálculo del tiempo de duplicación cambiado a cada 5 días.

**2020-04-27**: En la “Sala Situacional” se ha comenzado a publicar el
número de camas UCI disponibles y en uso.

Fuentes
-------

-   [Cuenta de twitter del MINSA](https://twitter.com/Minsa_Peru)
-   [Noticias del
    MINSA](https://www.gob.pe/busquedas?contenido%5B%5D=noticias&institucion%5B%5D=minsa&reason=sheet&sheet=1)
    -   [RSS de Noticias del
        MINSA](https://www.gob.pe/busquedas.rss?contenido%5B%5D=noticias&institucion%5B%5D=minsa)

Notas
-----

-   Códigos de UBIGEO de
    <a href="https://github.com/CONCYTEC/ubigeo-peru" class="uri">https://github.com/CONCYTEC/ubigeo-peru</a>
-   Códigos ISO-3166-2, usando el paquete en R `ISOcodes`:
    <a href="https://cran.r-project.org/package=ISOcodes" class="uri">https://cran.r-project.org/package=ISOcodes</a>
-   Mapa preliminar usando el paquete `mapview` en:
    <a href="https://castagnetto.site/peru/peru-covid-19-map.html" class="uri">https://castagnetto.site/peru/peru-covid-19-map.html</a>
-   Datos de población por departamento (al 2017):
    <a href="https://www.inei.gob.pe/estadisticas/indice-tematico/poblacion-y-vivienda/" class="uri">https://www.inei.gob.pe/estadisticas/indice-tematico/poblacion-y-vivienda/</a>
-   El [reporte N°29 del
    MINSA](https://www.gob.pe/institucion/minsa/noticias/109838-minsa-casos-confirmados-por-coronavirus-covid-19-son-395-en-peru-comunicado-n-29)
    corrige el número de casos confirmados en Huánuco del [reporte N°
    28](https://www.gob.pe/institucion/minsa/noticias/109810-minsa-casos-confirmados-por-coronavirus-covid-19-son-363-en-peru-comunicado-n-28)
-   El dataset de JHU
    (<a href="https://github.com/CSSEGISandData/COVID-19" class="uri">https://github.com/CSSEGISandData/COVID-19</a>),
    indica que Perú tiene 14 recuperados el día 2020-03-26
-   En el dashboard se han agregado gráficos de la trayectoria total de
    casos, gráficos del número de recuperados y fallecidos, y un mapa
    con la densidad (casos por millón de personas) por región.

Visualizaciones
---------------

-   [Dashboard interactivo sobre COVID-19 en el
    Perú](https://castagnetto.site/peru/dashboard-peru-covid-19.html)

Formato de datos
----------------

-   Los datos se están guardando en formatos abiertos exclusivamente,
    para asegurar la mayor compatibilidad posible: CSV y OpenDocument
    (ISO/IEC 26300-1:2015, ISO/IEC 26300-2:2015, ISO/IEC 26300-3:2015)

Estructura de los archivos CSV
------------------------------

**`covid-19-peru-data.csv`**

-   country: Peru (país)
-   iso3c: PER (código ISO de 3 letras para Perú)
-   region: Departamento del Perú (sólo a partir del 2020-03-13)
-   date: Fecha en formato ISO (YYYY-MM-DD)
-   confirmed: Casos confirmados
-   deaths: Decesos
-   recovered: Recuperados
-   negative\_cases: Casos descartados/negativos
-   pcr\_positivo: Casos detectados con pruebas moleculares
-   prueba\_rapida\_positivo: Casos detectados con pruebas serológicas
    (“pruebas rápidas”)

**`covid-19-peru-data-con-ubigeos.csv`**

-   country: Peru (país)
-   iso3c: PER (código ISO de 3 letras para Perú)
-   region: Departamento del Perú (sólo a partir del 2020-03-13)
-   cod\_dep\_inei: UBIGEO del departamenteo (INEI)
-   cod\_dep\_reniec: UBIGEO del departamenteo (RENIEC)
-   iso\_3166\_2\_code: Códigos ISO-3166-2 para el Departamento.
-   date: Fecha en formato ISO (YYYY-MM-DD)
-   confirmed: Casos confirmados
-   deaths: Decesos
-   recovered: Recuperados
-   negative\_cases: Casos descartados/negativos
-   pob\_2017: Población por departamento al 2017 (INEI)

**`covid-19-peru-fallecimientos.csv`**

-   fecha\_anuncio: Fecha en formato ISO (YYYY-MM-DD)
-   fecha\_fallecimiento: Fecha en formato ISO (YYYY-MM-DD)
-   fecha\_ingreso: Fecha en formato ISO (YYYY-MM-DD)
-   edad: en años
-   sexo: hombre/mujer
-   región: Departamento del Perú donde ocurrió el fallecimiento
-   viaje: País o región geográfica donde viajó la persona
-   contacto: Si la enfermadad se aquirió por contacto, la relación:
    amigo, familiar, etc.
-   contacto\_origen: Origne de la(s) persona(s) que contactaron y
    trajeron la enfermedad
-   lugar\_fallecimiento: hospital/casa/etc.
-   insuf\_resp: Si ingresó por insuficiencia respiratoria (1)
-   neumonia: Si ingresó por neumonía
-   otros\_síntomas: lista delimitada por “;” de otros síntomas
-   factores: si se conocen, otros factores (obesidad, asma, etc.)
-   misc: otra información
-   comunicado\_minsa: número del comunicado del MINSA

Información empleada para recolectar los datos
----------------------------------------------

Generales
---------

-   [Ministra de Salud exhortó a directores regionales implementar Plan
    Nacional por alerta mundial ante el
    COVID-19](https://www.gob.pe/institucion/minsa/noticias/84982-ministra-de-salud-exhorto-a-directores-regionales-implementar-plan-nacional-por-alerta-mundial-ante-el-covid-19)
    2020-02-25
-   [Ninguno de los 54 casos investigados ha resultado positivo por
    coronavirus](https://www.gob.pe/institucion/minsa/noticias/85190-ninguno-de-los-54-casos-investigados-ha-resultado-positivo-por-coronavirus)
    2020-02-28
-   [Ministerio de Salud aclara algunos mitos respecto al nuevo
    coronavirus
    Covid-19](https://www.gob.pe/institucion/minsa/noticias/85213-ministerio-de-salud-aclara-algunos-mitos-respecto-al-nuevo-coronavirus-covid-19)
    2020-02-29
-   [Minsa procesó 107 muestras por coronavirus COVID-19 y todas tienen
    resultado
    negativo](https://www.gob.pe/institucion/minsa/noticias/85332-minsa-proceso-107-muestras-por-coronavirus-covid-19-y-todas-tienen-resultado-negativo)
    2020-03-04
-   [Ministerio de Salud informa sobre resultado del procesamiento de
    muestras por coronavirus
    COVID-19](https://www.gob.pe/institucion/minsa/noticias/94105-ministerio-de-salud-informa-sobre-resultado-del-procesamiento-de-muestras-por-coronavirus-covid-19)
    2020-03-07
-   [Minsa brinda recomendaciones para la atención de una persona con
    coronavirus en
    casa](https://www.gob.pe/institucion/minsa/noticias/94095-minsa-brinda-recomendaciones-para-la-atencion-de-una-persona-con-coronavirus-en-casa)
    2020-03-07
-   [Número de nuevos casos de COVID – 19 está dentro de la curva
    esperada por
    autoridades](https://www.gob.pe/institucion/minsa/noticias/109581-numero-de-nuevos-casos-de-covid-19-esta-dentro-de-la-curva-esperada-por-autoridades)
    2020-03-19

Casos confirmados
-----------------

-   [Minsa procesó 155 muestras por coronavirus COVID-19 y una resultó
    positivo](https://www.gob.pe/institucion/minsa/noticias/108937-minsa-proceso-155-muestras-por-coronavirus-covid-19-y-una-resulto-positivo)
    2020-03-06
-   [Minsa procesó 219 muestras por coronavirus COVID-19 y 6 resultaron
    positivas](https://www.gob.pe/institucion/minsa/noticias/108938-minsa-proceso-219-muestras-por-coronavirus-covid-19-y-6-resultaron-positivas)
    2020-03-07
-   [Casos confirmados de coronavirus son importados y no existe
    transmisión
    comunitaria](https://www.gob.pe/institucion/minsa/noticias/94121-casos-confirmados-de-coronavirus-son-importados-y-no-existe-transmision-comunitaria)
    2020-03-08
-   [Minsa: Se elevaron a nueve los casos positivos por coronavirus
    COVID-19 tras analizarse 318
    muestras](https://www.gob.pe/institucion/minsa/noticias/108939-minsa-se-elevaron-a-nueve-los-casos-positivos-por-coronavirus-covid-19-tras-analizarse-318-muestras)
    2020-03-09
-   [Minsa: Se elevaron a once los casos positivos por coronavirus
    COVID-19 tras analizarse 346
    muestras](https://www.gob.pe/institucion/minsa/noticias/108940-minsa-se-elevaron-a-once-los-casos-positivos-por-coronavirus-covid-19-tras-analizarse-346-muestras)
    2020-03-10
-   [Minsa: Se elevaron a quince los casos positivos por coronavirus
    COVID-19 tras analizarse 656
    muestras](https://www.gob.pe/institucion/minsa/noticias/108943-minsa-se-elevaron-a-quince-los-casos-positivos-por-coronavirus-covid-19-tras-analizarse-656-muestras)
    2020-03-11
-   [Comunicado Oficial de Prensa - Coronavirus
    N°12](https://www.gob.pe/institucion/minsa/noticias/108935-comunicado-oficial-de-prensa-coronavirus-n-12)
    2020-03-15
-   [Comunicado Oficial de Prensa - Coronavirus
    N°13](https://www.gob.pe/institucion/minsa/noticias/108958-comunicado-oficial-de-prensa-coronavirus-n-13)
    2020-03-16
-   [Minsa: Casos confirmados por coronavirus COVID-19 ascienden a 117
    (Comunicado
    N° 15)](https://www.gob.pe/institucion/minsa/noticias/109438-minsa-casos-confirmados-por-coronavirus-covid-19-ascienden-a-117-comunicado-n-15)
    2020-03-17
-   [Minsa: Casos confirmados por coronavirus COVID-19 ascienden a 145
    (Comunicado
    N°17)](https://www.gob.pe/institucion/minsa/noticias/109467-minsa-casos-confirmados-por-coronavirus-covid-19-ascienden-a-145-comunicado-n-17)
    2020-03-18
-   [Minsa: Casos confirmados por coronavirus COVID-19 son 263 y se han
    producido 4 fallecidos (Comunicado
    N° 23)](https://www.gob.pe/institucion/minsa/noticias/109657-minsa-casos-confirmados-por-coronavirus-covid-19-son-263-y-se-han-producido-4-fallecidos-comunicado-n-23)
    2020-03-20
-   [Minsa: El Perú presenta 318 personas diagnosticadas y 5 fallecidas
    por COVID-19 (Comunicado
    N°27)](https://www.gob.pe/institucion/minsa/noticias/109792-minsa-el-peru-presenta-318-personas-diagnosticadas-y-5-fallecidas-por-covid-19-comunicado-n-27)
    2020-03-21
-   [Minsa: Casos confirmados por coronavirus COVID-19 son 395 en Perú
    (Comunicado
    N°29)](https://www.gob.pe/institucion/minsa/noticias/109838-minsa-casos-confirmados-por-coronavirus-covid-19-son-395-en-peru-comunicado-n-29)
    2020-03-23
-   [Minsa: Casos confirmados por coronavirus COVID-19 son 363 en Perú
    (Comunicado
    N° 28)](https://www.gob.pe/institucion/minsa/noticias/109810-minsa-casos-confirmados-por-coronavirus-covid-19-son-363-en-peru-comunicado-n-28)
    2020-03-22
-   [Minsa: Casos confirmados por coronavirus COVID-19 son 416 en Perú
    (Comunicado
    N°31)](https://www.gob.pe/institucion/minsa/noticias/109942-minsa-casos-confirmados-por-coronavirus-covid-19-son-416-en-peru-comunicado-n-31)
    2020-03-24
-   [Minsa: Casos confirmados por coronavirus COVID-19 son 480 en Perú
    (Comunicado
    N°33)](https://www.gob.pe/institucion/minsa/noticias/110065-minsa-casos-confirmados-por-coronavirus-covid-19-son-480-en-peru-comunicado-n-33)
    2020-03-25
-   [Minsa: Casos confirmados por coronavirus COVID-19 son 580 en Perú
    (Comunicado
    N°34)](https://www.gob.pe/institucion/minsa/noticias/111476-minsa-casos-confirmados-por-coronavirus-covid-19-son-580-en-peru-comunicado-n-34)
    2020-03-26
-   [Minsa: Casos confirmados por coronavirus COVID-19 son 635 en Perú
    (Comunicado
    N°36)](https://www.gob.pe/institucion/minsa/noticias/111543-minsa-casos-confirmados-por-coronavirus-covid-19-son-635-en-peru-comunicado-n-36)
    2020-03-27
-   [Minsa: Casos confirmados por coronavirus COVID-19 asciende a 671 en
    el Perú (Comunicado
    N°38)](https://www.gob.pe/institucion/minsa/noticias/111568-minsa-casos-confirmados-por-coronavirus-covid-19-asciende-a-671-en-el-peru-comunicado-n-38)
    2020-03-28
-   [Minsa: Casos confirmados por coronavirus Covid-19 ascienden a 852
    en el Perú (Comunicado
    N° 40)](https://www.gob.pe/institucion/minsa/noticias/111590-minsa-casos-confirmados-por-coronavirus-covid-19-ascienden-a-852-en-el-peru-comunicado-n-40)
    2020-03-29
-   [Minsa: Casos confirmados por Coronavirus COVID-19 asciende a 950 en
    el Perú (Comunicado
    N°41)](https://www.gob.pe/institucion/minsa/noticias/111623-minsa-casos-confirmados-por-coronavirus-covid-19-asciende-a-950-en-el-peru-comunicado-n-41)
    2020-03-30
-   [Minsa: Casos confirmados por coronavirus Covid-19 ascienden a 1065
    en el Perú (Comunicado
    N°44)](https://www.gob.pe/institucion/minsa/noticias/111653-minsa-casos-confirmados-por-coronavirus-covid-19-ascienden-a-1065-en-el-peru-comunicado-n-44)
    2020-03-31
-   [Minsa: Casos confirmados por coronavirus COVID-19 ascienden a 1323
    en el Perú (Comunicado
    N°46)](https://www.gob.pe/institucion/minsa/noticias/111718-minsa-casos-confirmados-por-coronavirus-covid-19-ascienden-a-1323-en-el-peru-comunicado-n-46)
    2020-04-01
-   [Minsa: Casos confirmados por Coronavirus COVID-19 ascienden a 1414
    en el Perú (Comunicado
    N°49)](https://www.gob.pe/institucion/minsa/noticias/111774-minsa-casos-confirmados-por-coronavirus-covid-19-ascienden-a-1414-en-el-peru-comunicado-n-499)
    2020-04-02
-   [Minsa: Casos confirmados por coronavirus Covid-19 ascienden a 2281
    en el Perú (Comunicado
    N°55)](https://www.gob.pe/institucion/minsa/noticias/111888-minsa-casos-confirmados-por-coronavirus-covid-19-ascienden-a-2281-en-el-peru-comunicado-n-55)
    2020-04-05
-   [Minsa: Casos confirmados por coronavirus COVID-19 ascienden a 2561
    en el Perú (Comunicado
    N°56)](https://www.gob.pe/institucion/minsa/noticias/111994-minsa-casos-confirmados-por-coronavirus-covid-19-ascienden-a-2561-en-el-peru-comunicado-n-56)
    2020-04-06
-   [Minsa: Casos confirmados por coronavirus COVID-19 ascienden a 2 954
    en el Perú (Comunicado
    N° 57)](https://www.gob.pe/institucion/minsa/noticias/112042-minsa-casos-confirmados-por-coronavirus-covid-19-ascienden-a-2-954-en-el-peru-comunicado-n-57)
    2020-04-07
-   [Minsa: Casos confirmados por coronavirus COVID-19 ascienden a 4 342
    en el Perú (Comunicado
    N°58)](https://www.gob.pe/institucion/minsa/noticias/112079-minsa-casos-confirmados-por-coronavirus-covid-19-ascienden-a-4-342-en-el-peru-comunicado-n-58)
    2020-04-08
-   [Minsa: Casos confirmados por coronavirus COVID-19 ascienden a 5 256
    en el Perú (Comunicado
    N°60)](https://www.gob.pe/institucion/minsa/noticias/112117-minsa-casos-confirmados-por-coronavirus-covid-19-ascienden-a-5-256-en-el-peru-comunicado-n-60)
    2020-04-09
-   [Minsa: Casos confirmados por coronavirus COVID-19 ascienden a 5 897
    en el Perú (Comunicado
    N°61](https://www.gob.pe/institucion/minsa/noticias/112148-minsa-casos-confirmados-por-coronavirus-covid-19-ascienden-a-5-897-en-el-peru-comunicado-n-61)
    2020-04-10
-   [Minsa: Casos confirmados por coronavirus COVID-19 ascienden a 6 848
    en el Perú (Comunicado
    N° 62)](https://www.gob.pe/institucion/minsa/noticias/112163-minsa-casos-confirmados-por-coronavirus-covid-19-ascienden-a-6-848-en-el-peru-comunicado-n-62)
    2020-04-11
-   [Minsa: Casos confirmados por Coronavirus COVID-19 ascienden a 7 519
    en el Perú (Comunicado
    N° 63)](https://www.gob.pe/institucion/minsa/noticias/112194-minsa-casos-confirmados-por-coronavirus-covid-19-ascienden-a-7-519-en-el-peru-comunicado-n-63)
    2020-04-12
-   [Minsa: Casos confirmados por coronavirus COVID-19 ascienden a 9 784
    en el Perú (Comunicado
    N°64)](https://www.gob.pe/institucion/minsa/noticias/112315-minsa-casos-confirmados-por-coronavirus-covid-19-ascienden-a-9-784-en-el-peru-comunicado-n-64)
    2020-04-13
-   [Minsa: Casos confirmados por Coronavirus COVID-19 ascienden a 10
    303 en el Perú (Comunicado
    N° 65)](https://www.gob.pe/institucion/minsa/noticias/112670-minsa-casos-confirmados-por-coronavirus-covid-19-ascienden-a-10-303-en-el-peru-comunicado-n-65)
    2020-04-14
-   [Minsa: Casos confirmados por coronavirus COVID-19 ascienden a 11
    475 en el Perú (Comunicado
    N° 66)](https://www.gob.pe/institucion/minsa/noticias/125568-minsa-casos-confirmados-por-coronavirus-covid-19-ascienden-a-11-475-en-el-peru-comunicado-n-66)
    2020-04-15
-   [Minsa: Casos confirmados por coronavirus COVID-19 ascienden a 12
    491 en el Perú ( Comunicado
    N°67)](https://www.gob.pe/institucion/minsa/noticias/126023-minsa-casos-confirmados-por-coronavirus-covid-19-ascienden-a-12-491-en-el-peru-comunicado-n-67)
    2020-04-16
-   [Minsa: Casos confirmados por coronavirus COVID-19 ascienden a 13
    489 en el Perú (Comunicado
    N° 68)](https://www.gob.pe/institucion/minsa/noticias/126083-minsa-casos-confirmados-por-coronavirus-covid-19-ascienden-a-13-489-en-el-peru-comunicado-n-68)
    2020-04-17
-   [Minsa: Casos confirmados por coronavirus COVID-19 ascienden a 14
    420 en el Perú (Comunicado
    N° 69)](https://www.gob.pe/institucion/minsa/noticias/126136-minsa-casos-confirmados-por-coronavirus-covid-19-ascienden-a-14-420-en-el-peru-comunicado-n-69)
    2020-04-18
-   [Minsa: Casos confirmados por coronavirus COVID-19 ascienden a 15
    628 en el Perú (Comunicado
    N° 70)](https://www.gob.pe/institucion/minsa/noticias/126658-minsa-casos-confirmados-por-coronavirus-covid-19-ascienden-a-15-628-en-el-peru-comunicado-n-70)
    2020-04-19
-   [Minsa: Casos confirmados por coronavirus COVID-19 ascienden a 16
    325 en el Perú ( Comunicado
    N° 72)](https://www.gob.pe/institucion/minsa/noticias/126686-minsa-casos-confirmados-por-coronavirus-covid-19-ascienden-a-16-325-en-el-peru-comunicado-n-72)
    2020-04-20
-   [Minsa: Casos confirmados por coronavirus COVID-19 ascienden a 17
    837 (Comunicado
    N° 73)](https://www.gob.pe/institucion/minsa/noticias/126735-minsa-casos-confirmados-por-coronavirus-covid-19-ascienden-a-17-837-comunicado-n-73)
    2020-04-21
-   [Minsa: Casos confirmados por Coronavirus COVID-19 ascienden a 19
    250 en el Perú (Comunicado
    N° 74)](https://www.gob.pe/institucion/minsa/noticias/127404-minsa-casos-confirmados-por-coronavirus-covid-19-ascienden-a-19-250-en-el-peru-comunicado-n-74)
    2020-04-22
-   [Minsa: Casos confirmados por coronavirus COVID-19 ascienden a 20
    914 en el Perú ( Comunicado
    N° 75)](https://www.gob.pe/institucion/minsa/noticias/127667-minsa-casos-confirmados-por-coronavirus-covid-19-ascienden-a-20-914-en-el-peru-comunicado-n-75)
    2020-04-23
-   [Minsa: Casos confirmados por coronavirus COVID-19 ascienden a 21
    648 en el Perú (Comunicado
    N° 76)](https://www.gob.pe/institucion/minsa/noticias/128059-minsa-casos-confirmados-por-coronavirus-covid-19-ascienden-a-21-648-en-el-peru-comunicado-n-76)
    2020-04-24
-   [Minsa: Casos confirmados por coronavirus COVID-19 ascienden a 25
    331 en el Perú ( Comunicado
    N° 77)](https://www.gob.pe/institucion/minsa/noticias/131646-minsa-casos-confirmados-por-coronavirus-covid-19-ascienden-a-25-331-en-el-peru-comunicado-n-77)
    2020-04-25
-   [Minsa: Casos confirmados por coronavirus COVID-19 ascienden a 27
    517 en el Perú (Comunicado
    N° 78)](https://www.gob.pe/institucion/minsa/noticias/131667-minsa-casos-confirmados-por-coronavirus-covid-19-ascienden-a-27-517-en-el-peru-comunicado-n-78)
    2020-04-26
-   [Minsa: Casos confirmados por coronavirus COVID-19 ascienden a 28
    699 en el Perú (Comunicado
    N° 79)](https://www.gob.pe/institucion/minsa/noticias/140641-minsa-casos-confirmados-por-coronavirus-covid-19-ascienden-a-28-699-en-el-peru-comunicado-n-79)
    2020-04-27
-   [Minsa: Casos confirmados por Coronavirus COVID-19 ascienden a 31
    190 en el Perú (Comunicado
    N° 80)](https://www.gob.pe/institucion/minsa/noticias/141088-minsa-casos-confirmados-por-coronavirus-covid-19-ascienden-a-31-190-en-el-peru-comunicado-n-80)
    2020-04-28

Recuperados
-----------

-   [Paciente cero con coronavirus fue dado de alta tras respetar
    aislamiento domiciliario
    recomendado](https://www.gob.pe/institucion/minsa/noticias/108961-paciente-cero-con-coronavirus-fue-dado-de-alta-tras-respetar-aislamiento-domiciliario-recomendado)
    2020-03-16
-   [Minsa: Casos confirmados por coronavirus COVID-19 son 635 en Perú
    (Comunicado
    N°36)](https://www.gob.pe/institucion/minsa/noticias/111543-minsa-casos-confirmados-por-coronavirus-covid-19-son-635-en-peru-comunicado-n-36)
    2020-03-27 (menciona el número de pacientes con alta)
-   [Minsa anuncia que 16 pacientes ya se han recuperado del
    Covid-19](https://www.gob.pe/institucion/minsa/noticias/111581-minsa-anuncia-que-16-pacientes-ya-se-han-recuperado-del-covid-19)
    2020-03-28

Fallecimientos
--------------

-   [Minsa lamenta el sensible fallecimiento del primer paciente a causa
    de infección COVID-19 (Comunicado
    N°20)](https://www.gob.pe/institucion/minsa/noticias/109580-minsa-lamenta-el-sensible-fallecimiento-del-primer-paciente-a-causa-de-infeccion-covid-19-comunicado-n-20)
    2020-03-19
    -   Hombre, 78 años, hipertensión, ingresó 2020-03-17 por
        insuficiencia respiratoria severa, falleció en hospital, Lima
-   [Minsa lamenta el sensible fallecimiento de dos personas por
    infección por COVID-19 (Comunicado
    N°21)](https://www.gob.pe/institucion/minsa/noticias/109603-minsa-lamenta-el-sensible-fallecimiento-de-dos-personas-por-infeccion-por-covid-19-comunicado-n-21)
    2020-03-19
    -   Hombre, 47 años, viaje a España, asma, obesidad, ingreso por
        insuficiencia respiratoria y shock séptico, falleció en
        hospital, Lima
    -   Hombre, 69 años, viaje a España, ingreso por cuadro
        respiratorio, falleció en domicilio, Lima
-   [Minsa lamenta el sensible fallecimiento de una persona por
    infección por COVID-19 (Comunicado
    N°22)](https://www.gob.pe/institucion/minsa/noticias/109639-minsa-lamenta-el-sensible-fallecimiento-de-una-persona-por-infeccion-por-covid-19-comunicado-n-22)
    2020-03-20
    -   Mujer, 75 años, viaje a España, ingreso por insuficiencia
        respiratoria y neumonía el 2020-03-19, falleció en hospital,
        Lima
-   [Minsa lamenta el sensible fallecimiento de una persona por
    infección por COVID-19 (Comunicado
    N°25)](https://www.gob.pe/institucion/minsa/noticias/109778-minsa-lamenta-el-sensible-fallecimiento-de-una-persona-por-infeccion-por-covid-19-comunicado-n-25)
    2020-03-21
    -   Hombre, 83 años, contacto con familiar procedente de Europa,
        ingreso por insuficiencia respiratoria y neumonía, falleció en
        hospital, Piura
-   [Minsa lamenta informar el sensible fallecimiento de dos personas
    por infección con COVID-19 (Comunicado
    N°30)](https://www.gob.pe/institucion/minsa/noticias/109930-minsa-lamenta-informar-el-sensible-fallecimiento-de-dos-personas-por-infeccion-con-covid-19-comunicado-n-30)
    2020-03-24
    -   Hombre, 38 años, obesidad, ingresó 2020-03-22 por insuficiencia
        respiratoria, falleció en hospital, Lima
    -   Mujer, 66 años, ingresó por insuficiencia respiratoria aguda y
        neumonía, falleció en hospital, La Libertad
-   [Minsa lamenta el sensible fallecimiento de dos personas por
    infección con Covid-19 (Comunicado
    N°32)](https://www.gob.pe/institucion/minsa/noticias/110050-minsa-lamenta-el-sensible-fallecimiento-de-dos-personas-por-infeccion-con-covid-19-comunicado-n-32)
    2020-03-25
    -   Hombre, 76 años, nacionalidad mexicana, insuficiencia
        respiratoria y comorbilidad, diabetes y enfermedad cardíaca
        preexistente, falleció en hospital, Cusco
    -   Home, 94 años, insuficiencia renal y bronquitis crónica,
        diabetes, falleció en hospital, Lima
-   [Minsa lamenta informar el sensible fallecimiento de dos personas
    por infección con COVID-19 (Comunicado
    N°35)](https://www.gob.pe/institucion/minsa/noticias/111529-minsa-lamenta-informar-el-sensible-fallecimiento-de-dos-personas-por-infeccion-con-covid-19-comunicado-n-35)
    2020-03-27
    -   Hombre, 56 años, insuficiencia respiratoria aguda-grave, ingresó
        el 2020-03-26 y falleció el mismo día en el hospital, La
        Libertad
    -   Hombre, 65 años, ingresó el 2020-03-21, falleció en el hospital
        el 2020-03-26, Lima
-   [Minsa lamenta informar el sensible fallecimiento de cinco personas
    por infección con COVID-19 (Comunicado
    N°37)](https://www.gob.pe/institucion/minsa/noticias/111566-minsa-lamenta-informar-el-sensible-fallecimiento-de-cinco-personas-por-infeccion-con-covid-19-comunicado-n-37)
    2020-03-28
    -   Hombre, 50 años, insuficiencia respiratoria aguda y neumonía,
        falleció en el hospital el 2020-03-26, Lambayeque
    -   Hombre, 66 años, insuficiencia respiratoria, sepsis y neumonía,
        falleció en el hospital el 2020-03-26, Lima
    -   Hombre, 43 años, insuficiencia respiratoria, sepsis y neumonía,
        obesidad, falleció en el hospital el 2020-03-27, Lima
    -   Hombre, 64 años, procedente de Hong Kong, falleció en su
        domicilio el 2020-03-27, Cusco
    -   Mujer, 60 años, insuficiencia respiratoria, shock séptico y
        neumonía, falleció en el hospital el 2020-03-27, Callao
-   [Minsa lamenta el sensible fallecimiento de dos personas por
    infección con COVID-19 (Comunicado
    N° 39)](https://www.gob.pe/institucion/minsa/noticias/111587-minsa-lamenta-el-sensible-fallecimiento-de-dos-personas-por-infeccion-con-covid-19-comunicado-n-39)
    2020-03-29
    -   Hombre, 91 años, neumonía, enfermedad renal crónica, falleció en
        el hospital el 2020-03-27, Lima
    -   Mujer, 66 años, neumonía, obesidad mórbida, falleción en
        hospital el 2020-03-28, Ancash
-   [El Ministerio de Salud lamenta informar el sensible fallecimiento
    de seis personas por infección con COVID-19
    (Comunicado 42)](https://www.gob.pe/institucion/minsa/noticias/111625-el-ministerio-de-salud-lamenta-informar-el-sensible-fallecimiento-de-seis-personas-por-infeccion-con-covid-19-comunicado-42)
    2020-03-30
    -   Hombre, 63 años, neumonía, obesidad, comorbilidad, diabetes
        mellitus y tuberculosis previa, falleció en el hospital el
        2020-03-30, Loreto.
    -   Mujer, 58 años, neumonía, antecedentes de neumonía, falleció en
        el hospital el 2020-03-29, Callao.
    -   Hombre, 56 años, obesidad, falleció en el hospital el
        2020-03-30, Loreto.
    -   Mujer, 81 años, neumonía, shock séptico, diabetes mellitus,
        falleció en el hospital el 2020-03-28, Lima.
    -   Mujer, 76 años, neumonía, antecedentes de HTA y desnutrición
        crónica, ingresó el 2020-03-26, falleció en el hospital el
        2020-03-29. Lima
    -   Mujer, 76 años, neumonía, enfermedaes preexistentes, ingresó el
        2020-03-26, falleció en el hospital el 2020-03-29. Lima
-   [Minsa lamenta el sensible fallecimiento de seis personas por
    infección con COVID-19 (Comunicado
    N°45)](https://www.gob.pe/institucion/minsa/noticias/111655-minsa-lamenta-el-sensible-fallecimiento-de-seis-personas-por-infeccion-con-covid-19-comunicado-n-45)
    2020-03-31
    -   Hombre, 26 años, neumonía, asma y obesidad, ingresó el
        2020-03-29, falleció en el hospital el 2020-03-29, Callao.
    -   Mujer, 74 años, neumomía, insuficiencia renal crónica y cirrosis
        hepática, ingresó el 2020-03-29, falleció en el hospital el
        2020-03-29, Lima.
    -   Hombre, 46 años, neumonía crónica, lumbalgia y alto consumo de
        alcohol, falleció el 2020-03-30 en su domicilio, Tumbes.
    -   Hombre, 53 años, neumonía crónica, ingresó el 2020-03-23,
        falleció en el hospital el 2020-03-30. Lima.
    -   Hombre, 60 años, infección respiratoria, neumonía atípica y
        shock séptico, ingresó el 2020-03-26, falleció en el hospital el
        2020-03-30, Lima.
    -   Hombre, 66 años, neumonía crónica, falleció en el hospital el
        2020-03-31, San Martín.
-   [Minsa lamenta el sensible fallecimiento de ocho personas por
    infección con COVID-19 (Comunicado
    N°47)](https://www.gob.pe/institucion/minsa/noticias/111724-minsa-lamenta-el-sensible-fallecimiento-de-ocho-personas-por-infeccion-con-covid-19-comunicado-n-47)
    2020-04-01
    -   Hombre, 75 años, neumonía, hipertensión y enfermedad cerebro
        cardiovascular, falleció el 2020-03-27 en el hospital, Lima.
    -   Hombre, 96 años, neumonía, falleció el 2020-03-29 en el
        hospital, Lima.
    -   Mujer, 83 años, neumonía, falleció el 2020-03-29 en el hospital,
        Lima.
    -   Hombre, 87 años, neumonía, hipertensión y enfermedad cerebro
        cardiovascular, falleció el 2020-03-29 en el hospital, Lima.
    -   Mujer, 59 años, neumonía, fibrosis pulmonar, falleció el
        2020-03-30 en el hospital, Lambayeque.
    -   Hombre, 60 años, neumonía, hipertensión y diabetes mellitus,
        falleció el 2020-03-30 en el hospital, Lima.
    -   Hombre, 73 años, neumonía, falleció el 2020-03-31 en el
        hospital, Callao.
    -   Hombre, 68 años, neumonía, falleció el 2020-03-31 en el
        hospital, Lima.
-   [Minsa lamenta el sensible fallecimiento de nueve personas por
    infección con COVID-19 (Comunicado
    N°48)](https://www.gob.pe/institucion/minsa/noticias/111750-minsa-lamenta-el-sensible-fallecimiento-de-nueve-personas-por-infeccion-con-covid-19-comunicado-n-48)
    2020-04-01
    -   Mujer, 69 años, insuficiencia respiratoria, diabetes mellitus e
        hipertensión arterial, falleció el 2020-03-29 en el hospital,
        Lambayeque.
    -   Hombre, 68 años, neumonía, falleció en el hospital el
        2020-03-31, Lima.
    -   Hombre, 60 años, neumonía, falleció en el hospital el
        2020-03-31, Lima.
    -   Mujer, 63 años, neumonía, falleció en el hospital el 2020-03-31,
        Lima.
    -   Hombre, 59 años, neumonía, falleció en el hospital el
        2020-03-31, Lima.
    -   Hombre, 26 años, insuficiencia respiratoria y neumonía, falleció
        en el hospital el 2020-03-30, Lima.
    -   Hombre, 89 años, insuficiencia respiratoria y neumonía, falleció
        en el hospital el 2020-03-31, Arequipa.
    -   Hombre, 59 años, insuficiencia cardiorrespiratoria, diabetes
        mellitus y hemodializado, falleció en el hospital el 2020-03-31,
        La Libertad.
    -   Mujer, 65 años, sintomatología respiratoria, obesidad y
        diabetes, falleció en el hospital el 2020-03-31, Lima.
-   [Minsa lamenta el sensible fallecimiento de ocho personas por
    infección con COVID-19 (Comunicado
    N°50)](https://www.gob.pe/institucion/minsa/noticias/111777-minsa-lamenta-el-sensible-fallecimiento-de-ocho-personas-por-infeccion-con-covid-19-comunicado-n-50)
    2020-04-02
    -   Hombre, 57 años, insuficiencia respiratoria y neumonía, falleció
        en el hospital 2020-03-30, Junín.
    -   Hombre, 77 años, insuficiencia respiratoria y neumonía, falleció
        en el hospital el 2020-03-31, Lima.
    -   Mujer, 73 años, neumonía, contacto con familiar positivo a
        COVID-19. falleció en el hospital el 2020-04-01, Lima.
    -   Mujer, 58 años, neumonía, hipertensión arterial, falleció en el
        hospital el 2020-04-01, Tumbes.
    -   Hombre, 73 años, diabetes mellitus, hipertensión arterial e
        insuficiencia renal, falleció en el hospital el 2020-04-01,
        Lima.
    -   Hombre, 60 años, infección respiratoria aguda y neumonía,
        falleció en el hospital el 2020-04-01, Lima.
    -   Hombre, 65 años, neumonía y shock séptico, falleció en el
        hospital el 2020-04-01, Lima.
    -   Mujer, 67 años, insuficiencia respiratoria aguda, obesidad,
        falleció en el hospital el 2020-04-01, Lima.
