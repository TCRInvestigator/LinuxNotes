# Get the transcript ID from the command line argument if
len(sys.argv) != 2: 
  print("Usage: python fetch_protein.py <transcript_id>") 
  sys.exit(1)

transcript_id = sys.argv[1]
print(fetch_protein_sequence(transcript_id))
