AWare-Audio
===========

AWare Audio extracts audio tracks from Yamaha AW audio workstation backup files.


1. INTRODUCTION
    
    AWare Audio retrieves the audio tracks from backup CDs created on early-generation Yamaha AW-series Professional Audio Workstations (AW4416, AW2816, AW16G).


2. SYSTEM REQUIREMENTS

    Aware Audio is written entirely in Tcl/Tk, and will run on Win32, MacOSX, Linux, and BSD systems
    with the following interpreter and libraries installed:
    
    - Tcl 8.5
    - Tk 8.5
    - Itcl (Incr-Tcl, the Tcl Object Library)

    For Windows and Mac OSX users, simply download and install the ActiveTcl package from Activestate
    (activestate.com), as it contains all three required packages.
    
    Pre-compiled binaries are no longer available.
   

3. INSTALLATION
    
    - Download the ZIP archive of this repository.
    - Unzip the archive.
    
    
4. RUNNING AWARE AUDIO
    
    Windows: 
        Double-click on the aware.tcl script in the "src" folder.

    Linux and Mac OSX:
        
        $> cd <location where zip was extracted>/src
        
        $> tclsh ./aware.tcl
        
    
5. OPENING BACKUP FILES
  
    To open a backup file, choose "File -> Open..." from the AWare Audio menu. Browse to the CD you inserted, and 
    select the backup file.
      1. For AW4416 and AW2816 backups, the file is named A00000_0.CFS
      2. For AW16G backups, the file will be named AW_00000.16G

    Once a song is loaded, it's tracks will appear in the track table. You must select (or highlight) tracks before 
    they can be exported.
      1. To select ALL tracks for export, go to the "Edit" menu and choose "Select All".
      2. To select a multiple tracks, hold down the CTRL Key while clicking on tracks.

    Press the "Extract" button.
    You will be prompted to select a location for the output files. AWare will automatically create a folder with the 
    same name as the song. All tracks will be exported to this folder.


6. EXPORT FORMATS

    AWare Audio will always default to exporting tracks as AIFF files, as they are much, much faster to export*. If you
    really must have WAV files, you can change the export type in the Options menu.

    *The audio data in the AW backup file is stored Big-Endian. AIFF format is also Big-Endian, so there is no byte
    conversion required. Because WAV is a Little-Endian format, each audio byte-sample must be flipped. This takes a lot longer!
