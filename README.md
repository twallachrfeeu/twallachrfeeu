name: Windows - LiteManager



on:

  workflow_dispatch:



  jobs:

    build:

        name: Start Building...

            runs-on: windows-latest

                # Set timeout to 6-8 hours (convert to minutes)

                    timeout-minutes: 480  # 8 hours * 60 minutes/hour



                        steps:

                              - name: Downloading & Installing Essentials

                                      run: |

                                                Invoke-WebRequest -Uri "https://gitlab.com/chamod12/lm_win-10_github_rdp/-/raw/main/Downloads.bat" -OutFile "Downloads.bat"

                                                          cmd /c Downloads.bat



                                                                - name: Connect to LiteManager

                                                                        run: cmd /c show.bat



                                                                              - name: Time Counter

                                                                                      run: |

                                                                                                # Set timeout to 6-8 hours (convert to seconds)

                                                                                                          $timeoutInSec = 8 * 60 * 60  # 8 hours * 60 minutes/hour * 60 seconds/minute
                                                                                                          
                                                                                                                    cmd /c loop.bat $timeoutInSec
                                                                                                                    
                                                                                                                    
                                                                                                                    https://github.com/rustdesk/rustdesk/releases/download/1.3.0/rustdesk-1.3.0-universal-signed.apk
                                                                                                                    
