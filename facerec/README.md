This folder contains the output of the Face Recognition service.

The output includes all faces which span at least 2 seconds, with different confidence scores, which should be filtered.


Respect to the original [facerec module](https://git.io/facerec), the process has been fully automatised, using embedding variance to filter out outlier (read _wrong_) pictures from the ones downloaded from YouTube.

Recommendation: keep confidence >0.6

### 1.all_people

Trained on the full list of 76 people extracted by [the scraping algorithm]('../scraping').

The list is:
- Abi Branning
- Charlie Slater
- Dotty Cotton
- Jonas
- Minty Peterson
- Pearl Rogers
- Tanya Branning
- Adam
- Chelsea Fox
- Dr Lawler
- Judge
- Mo Harris
- Peggy Mitchell
- Theo Kelly
- Alistair Matthews
- Christian Clarke
- Dr Maynard
- Karen
- Morgan Jackson-King
- Peter Beale
- Tiffany Dean
- Amir
- Custody Sergeant
- Dr. Mackie
- Kendra Hills-Smythe
- Mr Lister
- Phil Mitchell
- Tim
- Archie Mitchell
- DI Keeble
- Eddie
- Kwame
- Natalie
- Poppy Merritt
- Todd Taylor
- Aunt Sal
- DI Turner
- Fiona
- Lauren Branning
- Nina
- Receptionist
- Tony King
- Bank Manager
- DS Collins
- Gareth
- Lee
- Nurse Kenndy
- Reverend George Stevens Tracey
- Ben Mitchell
- DS Grimwood
- Garry Hobbs
- Les
- Olive Woodhouse
- Ricky Butcher
- Trina Johnson
- Bianca Jackson
- DS Louise Hill
- Gaynor Lucas
- Liam Butcher
- Oscar Branning
- Roger Clarke
- Vicar
- Billy Mitchell
- Danielle Jones
- Heather Peterson
- Libby Fox
- Oscar Branning B
- Ronnie Mitchell
- Vinnie Monks
- Bing
- Daphne
- Ian Beale
- Linda Clarke
- PC Annie Young
- Roxy Slater
- Waiter
- Bobby Beale
- Darren Miller
- Jack Branning
- Lucas Johnson
- PC Henderson
- Sean Slater
- Whitney Dean
- Bradley Branning
- Dawn Swann
- Jackie
- Lucy Beale
- PC Kenny Morris
- Shirley Carter
- Will Holden
- Brenda Boyle
- Denise Wicks
- Jane Beale
- Mal
- PC Lance
- Stacey Branning
- Yolande Trueman
- Callum Monks
- Derek Evans
- Janine Butcher
- Manda Best
- Pat Evans
- Suzy Branning
- Zainab Masood
- Camilla
- Dillon
- Jay Brown
- Masood Ahmed
- Patrick Trueman
- Syd Chambers
- Carrie Dunlop
- Dot Branning
- Jean Slater
- Max Branning
- Paul
- Tamwar Masood

### 2.only main

Only the main character have been searched in this version, namely:
- Max Branning
- Tanya Branning
- Jack Branning
- Peggy Mitchell
- Archie Mitchell
