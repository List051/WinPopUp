WinPopUp
WinPopUp è una libreria .NET che permette di associare popup informativi ai controlli di un form Windows Forms.
Installazione
Per utilizzare WinPopUp nel tuo progetto:
Clona o scarica il repository.
Aggiungi la libreria WinPopUp.dll al tuo progetto tramite Riferimenti.
Importa la libreria nel tuo codice.

Imports System.IO

' la libreria deve essere importata con Imports WinPopUp
Public Class Form1
    Private Sub Form1_Load(sender As Object, e As EventArgs) Handles MyBase.Load
        Try

            ' Carica le immagini dalle risorse (My.Resources)
            Dim imgInfo As Image = My.Resources.cashier  ' Nome dell'immagine senza estensione
            Dim imgWarning As Image = My.Resources.calculator_50

            ' Associa i popup ai pulsanti
            PopupHelper.AttachPopup(Button1, "Informazioni utili" & vbCr & "altre informazioni", imgInfo)
            PopupHelper.AttachPopup(Button2, "Attenzione! Controlla i dati", imgWarning)
        Catch ex As Exception
            MessageBox.Show("Errore nel caricamento delle immagini: " & ex.Message)
        End Try
    End Sub
End Class

Funzionalità
Associazione di popup personalizzati ai controlli.
Supporto per immagini personalizzate nei popup.
Facile integrazione con Windows Forms.
Requisiti
.NET Framework 4.5 o superiore
Visual Studio per lo sviluppo
Contribuire
Se vuoi contribuire al progetto, effettua un fork del repository, crea un branch con le tue modifiche e invia una pull request.
Licenza
Questo progetto è rilasciato sotto la licenza MIT. Per maggiori dettagli, consulta il file LICENSE.
Contatti
Per domande o suggerimenti, puoi aprire un'issue su GitHub oppure contattarmi direttamente.
Buon coding! 🚀
