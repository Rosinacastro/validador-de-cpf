# validador-de-cpf

export class Validacoes {
  static ValidaCpf(controle: AbstractControl) {
    const cpf = controle.value;

    let valido: boolean;

      valido = validate(cpf);

    if (valido) return null;

    return { cpfInvalido: true };
  }
}


////importa 

import { validate } from 'gerador-validador-cpf';



///////chama na função

cpf: new FormControl(null, [Validators.required,Validators.minLength(11),Validators.maxLength(11),Validacoes.ValidaCpf]),
