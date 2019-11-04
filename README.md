# spell_checker
Function is detecting words for spellcheck.


                from spellchecker import SpellChecker

                spell = SpellChecker()

                def create_list(s):
                    misp=[]
                    for words in s.casefold().split():
                  misp.append(words)
                    return misp

                def word_check(str_word):
                    misspelled = spell.unknown(str_word)
                    for word in misspelled:
                        if word != spell.correction(word):
                            suggestion=spell.correction(word)
                            print(f'Did you mean {"," .join(suggestion)} instead of {word}?')

                str_in=input('Input string : ')
                str_to_word=create_list(str_in)
                word_check(str_to_word)
