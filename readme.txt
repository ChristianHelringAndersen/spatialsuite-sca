--------------------
Modul til visning af kloakbr�nde og -ledninger fra SCA - Spildevandscenter Aved�re
-------------------- 

INSTALLATION :

1:   Install�r modulet
1.a: Kopi�r modulet "sca" til sitets moduler, dvs. til "[cbinfo.config.dir]/modules/custom/sca"
1.b: Skriv f�lgende entry i [cbinfo.modules]: <module name="sca" dir="custom/sca" permissionlevel="public"/>

2:   Rediger Profil(er)
2.a: Tilf�j et eller flere af temaerne til profilen.
2.b: Det kan evt. g�res vha. includes af hhv. temagruppe og temaer:
     
	2.6 eller tidligere:

		<include mustexist="false" nodes="/profile/themegroups/*" src="[module:sca.dir]/profiles/profile.xml"/>
        <include mustexist="false" nodes="/profile/themes/*" src="[module:sca.dir]/profiles/profile.xml"/>
		
      
3:   Rediger targetsets
3.a: Tilf�j det target, der findes skabelonen i targetset.xml under mappen "queries"
     hvor de mulige targets med tilh�rende referencer til datasource, temafil og presentation.
     Det kan evt. tilf�jes vha. include:
        <include src="[module:sca.dir]/queries/targetset.xml" nodes="/spatialqueries/targetset/*" mustexist="false"/>

4:	 Tilf�j signatur
4.a: Billeder i /images kopieres til /resources/symbols/custom/images/custom

4.b: F�lgende s�ttes ind i symbols3_5.txt

SYMBOL
    NAME 'bassin'
    TYPE PIXMAP
    IMAGE 'custom/images/custom/bassin.png'
END

SYMBOL
    NAME 'broend'
    TYPE PIXMAP
    IMAGE 'custom/images/custom/broend.png'
END

SYMBOL
    NAME 'fordelerbygvaerk'
    TYPE PIXMAP
    IMAGE 'custom/images/custom/fordelerbygvaerk.png'
END

SYMBOL
    NAME 'maalerbygvaerk'
    TYPE PIXMAP
    IMAGE 'custom/images/custom/maalerbygvaerk.png'
END

SYMBOL
    NAME 'overloeb'
    TYPE PIXMAP
    IMAGE 'custom/images/custom/overloeb.png'
END

SYMBOL
    NAME 'pumpestation'
    TYPE PIXMAP
    IMAGE 'custom/images/custom/pumpestation.png'
END

SYMBOL
    NAME 'reguleringsbygvaerk'
    TYPE PIXMAP
    IMAGE 'custom/images/custom/reguleringsbygvaerk.png'
END

SYMBOL
    NAME 'renseanlaeg'
    TYPE PIXMAP
    IMAGE 'custom/images/custom/renseanlaeg.png'
END

SYMBOL
    NAME 'sandfang'
    TYPE PIXMAP
    IMAGE 'custom/images/custom/sandfang.png'
END

SYMBOL
    NAME 'tilslutning_af_stik'
    TYPE PIXMAP
    IMAGE 'custom/images/custom/tilslutning_af_stik.png'
END

SYMBOL
    NAME 'tryktaarn'
    TYPE PIXMAP
    IMAGE 'custom/images/custom/tryktaarn.png'
END

SYMBOL
    NAME 'udloeb'
    TYPE PIXMAP
    IMAGE 'custom/images/custom/udloeb.png'
END

SYMBOL
    NAME 'udskiller'
    TYPE PIXMAP
    IMAGE 'custom/images/custom/udskiller.png'
END

SYMBOL
    NAME 'gulhus'
    TYPE PIXMAP
    IMAGE 'custom/images/custom/gulhus.png'
END

AFH�NGIGHEDER:

CBkort 2.6+

BEM�RKNINGER:

18-10-2011

I temaet 'br�nde' udstilles ogs� punkter som indikerer hvor stikledningen g�r ind p� privat grund. Pt. er det ikke muligt at filtre disse data fra. SCA er opm�rksomme p� problemet.

VERSIONSHISTORIK

14-11-2012

Modul opdateret s� knudetemaet viser de korrekte signaturer.

3-6-2013

Clientlayers tilf�jet, s� data vises direkte i browseren.