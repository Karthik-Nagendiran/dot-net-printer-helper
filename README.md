# dot-net-printer-helper
# C# Printer Helper class
A replica of Microsoft's Printer Helper class.
This will help in sending our custom content either a string or a stream or a file to the printer from any dot net application.

# Usage
```
  private void PrintString()
  {
      PrintDialog pd = new PrintDialog
      {
          PrinterSettings = new PrinterSettings()
      };
      
      if (DialogResult.OK == pd.ShowDialog(this))
      {
          string strToPrint = "This is the sample string to print";        
          RawPrinterHelper.SendStringToPrinter(pd.PrinterSettings.PrinterName, strToPrint);
          MessageBox.Show("Print Successful.");
      }
  }
```
