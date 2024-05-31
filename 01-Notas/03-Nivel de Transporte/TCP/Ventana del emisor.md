#flashcards/tcp 
#review2 

- La ventana del emisor (VE) es el número de octetos que una entidad puede transmitir, sin esperar ACKs, teniendo en cuenta el [[Control de flujo en TCP]] y [[Control de congestión en TCP]] a la vez:
	- VE = min(Ventana de congestión, Ventana de recepción[^1])=min(VC,VR)
- La VE indica el número máximo de octetos que pueden ser transmitidos, pero es interesante usar una variable auxiliar para contabilizar el número de octetos que se encuentran en el [[Buffer del emisor en TCP]] pendientes de ser asentidos, al que llamaremos OE (octetos enviados). De esta forma:
	- OE = UltimoOctetoEnviado - UltimoOctetoReconocido ≤ VE = min(VC, VR)
	- OE ≤ VE

[^1]: es importante recordar que ambas entidades tienen sus propias ventanas de congestión y recepción. En este caso, la VE de una entidad TCP se calcula como el mínimo entre la VC local y la VR que reporta la otra entidad utilizando el campo [[Ventana de recepción en TCP]]