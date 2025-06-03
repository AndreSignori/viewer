# viewer

Implementare questo codice : 

    public  class Criptatore
    {
         byte[] data;
         
         public Criptatore()
        {
            data = new byte[0];
        }

        public  void estrai_data(string file_da_criptare)
        {


           //vorremmo utilizzare matroska
        }


        public  void cripta_file(string file_da_criptare, string file_criptato, out byte[] key)
        {

            using (Aes cripter = Aes.Create())
            {
                cripter.KeySize = 256; // AES-256
                cripter.GenerateKey();
                key = cripter.Key;

                
               // cripter.Mode = CipherMode.GMC;
                cripter.Padding = PaddingMode.PKCS7;
                cripter.GenerateIV(); 

            }

        }
        public  void decripta_file(string file_criptato, out byte[] key)
        {
            key = new byte[0];

        }

    }
