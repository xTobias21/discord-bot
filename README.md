const Discord = erforderlich ( "discord.js" ) ;
const client =  neuer Discord.Client ( ) ;​
const token =  "TOKEN-HIER-EINSETZEN" ;
const Präfix =  "!"
 
client.on ( "bereit" , ( ) = > {   
    console.log ( " Moin , bin online" )
 
 
    client.user.setActivity ( `$ { prefix } ping | Ich bin nur fürs Video an` , { type : "PLAYING " } )
 
 
} ) ;
 
client.on ( 'Nachricht' , Nachricht = > { 
    wenn ( Nachricht.Inhalt.beginntMit ( Präfix + " Ping " ) )​
    {
        message.channel . send ( "Pong :ping_pong: \n Das hat " + client.ws . ping + " ms gedauert. " )
    }
 
    sonst  wenn ( Nachricht.Inhalt === ` < @ $ { Client.Benutzer.Name } > ` || Nachricht.Inhalt === ` <  @ ! $ { Client.Benutzer.ID } > ` ) {​​​​​ 
        message.channel.send ( ` `Hallo , mein Präfix ist : $ { prefix } ` ) ;
    }
    sonst  wenn ( Nachricht.Inhalt.beginntmit ( Präfix + " sagen " ) )​
    {
        const args = Nachricht.Inhalt.Slice ( 5 ) .Split ( " " ) ;​​​
        const saymessage1 = args.join ( "  " ) ;
        Nachricht. Kanal . Senden ( { Einbetten :  {
            Farbe :  ( Nachricht.Gilde.ich.displayHexColor ) ,​​​​​
            title :   `gesendet von $ { message. Autor . Benutzername } ` ,
            Beschreibung : saymessage1 ,
            Zeitstempel :  neues  Datum ( ) ,
            Fußzeile :  {
              Text : „ $ { Nachricht.Gilde.Name } “​​
            }
          }
        } ) ;
 
        
    }
} )
 
Kunde.Anmeldung ( Token ) ;
