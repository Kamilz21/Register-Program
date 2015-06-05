# Register-Program
This program is coded in Visual Basic and is a working Cash Register.
//Code For Register Program// Programed in Visual Studios//

Public Class Form1
    Dim cost As Double
    Dim tax As Double
    Dim totalcost As Double
    Dim total As Double
    Dim fmtStr As String = "{0,-10}{1,25:C}"

    Private Sub Button1_Click(sender As System.Object, e As System.EventArgs) Handles Button1.Click
        cost = CDbl(txtcost.Text)
        txtreciept.Items.Add(String.Format(fmtStr, cmbox.SelectedItem, cost))
        totalcost = totalcost + cost
    End Sub

    Private Sub Button3_Click(sender As System.Object, e As System.EventArgs) Handles Button3.Click
        txtreciept.Items.Clear()
    End Sub

    Private Sub Button2_Click(sender As System.Object, e As System.EventArgs) Handles Button2.Click
        tax = totalcost * 0.07
        total = totalcost + tax
        txtreciept.Items.Add(String.Format(fmtStr, "   ", "--------------------"))
        txtreciept.Items.Add(String.Format(fmtStr, "Total", totalcost))
        txtreciept.Items.Add(String.Format(fmtStr, "Tax", tax))
        txtreciept.Items.Add(String.Format(fmtStr, "Cost", total))
    End Sub

    Private Sub Form1_Load(sender As Object, e As EventArgs) Handles MyBase.Load

    End Sub

    Private Sub cmbox_SelectedIndexChanged(sender As Object, e As EventArgs) Handles cmbox.SelectedIndexChanged

    End Sub
End Class
