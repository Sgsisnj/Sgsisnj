d['password'] ) ): 
                       outputFile.write( '{}={}\n'.format(d['account'], cdw) )
                       encryptedPasswords.remove( d ) 
                       outputFile.flush() 
                # check reversed capsDigitWords
                for d in encryptedPasswords:
                   if( check_pass( cdRw, d['password'] ) ): 
                       outputFile.write( '{}={}\n'.format(d['account'], cdRw) )
                       encryptedPasswords.remove( d ) 
                       outputFile.flush()             
    # crack the reversed versions of the previous capsDigitWords
    #for d in encryptedPasswords: 
    #    for w in words:
    #        rw = transform_reverse( w )[1] # reverse the word
    #        digitReversedWords = transform_digits( rw )
    #        digitReversedWords.pop() # last item in list is plain reversed word
    #        for drw in digitReversedWords:
    #            capsDigitReversedWords = transform_capitalize(drw)
    #            for cdrw in capsDigitReversedWords:
    #                if( check_pass( cdrw, d['password'] ) ): 
    #                    outputFile.write( '{}={}\n'.format(d['account'],cdrw) )
    #                encryptedPasswords.remove( d ) 
    #                outputFile.flush()
    # End crack_pass function
    outputFile.close()

    
