# translate-datePicker-primeNg-v19
Tradução do component p-datePicker do primeNG, funciona na última versão v19, a única testada.

# Crie um arquivo para ser usado globalmente, exemplo: src\app\utils\primeng-pt.config.ts
```typescript
import { PrimeNG } from "primeng/config"; 

export function setPtBrPrimeNgConfig(config: PrimeNG) {
  config.setTranslation({
    startsWith: 'Começa com',
    contains: 'Contém',
    notContains: 'Não contém',
    endsWith: 'Termina com',
    equals: 'Igual',
    notEquals: 'Diferente',
    noFilter: 'Sem filtro',
    lt: 'Menor que',
    lte: 'Menor ou igual a',
    gt: 'Maior que',
    gte: 'Maior ou igual a',
    is: 'É',
    isNot: 'Não é',
    before: 'Antes',
    after: 'Depois',
    apply: 'Aplicar',
    matchAll: 'Corresponder a todos',
    matchAny: 'Corresponder a qualquer',
    addRule: 'Adicionar regra',
    removeRule: 'Remover regra',
    accept: 'Sim',
    reject: 'Não',
    choose: 'Escolher',
    upload: 'Enviar',
    cancel: 'Cancelar',
    dayNames: ['Domingo', 'Segunda-feira', 'Terça-feira', 'Quarta-feira', 'Quinta-feira', 'Sexta-feira', 'Sábado'],
    dayNamesShort: ['Dom', 'Seg', 'Ter', 'Qua', 'Qui', 'Sex', 'Sáb'],
    dayNamesMin: ['D', 'S', 'T', 'Q', 'Q', 'S', 'S'],
    monthNames: ['Janeiro', 'Fevereiro', 'Março', 'Abril', 'Maio', 'Junho', 'Julho', 'Agosto', 'Setembro', 'Outubro', 'Novembro', 'Dezembro'],
    monthNamesShort: ['Jan', 'Fev', 'Mar', 'Abr', 'Mai', 'Jun', 'Jul', 'Ago', 'Set', 'Out', 'Nov', 'Dez'],
    today: 'Hoje',
    clear: 'Limpar',
    weekHeader: 'Sm'
  });
}
```
# Seu AppComponent

```typescript
import { setPtBrPrimeNgConfig } from './utils/primeng-pt.config';

@Component({
  selector: 'app-root',
  imports: [
    RouterOutlet
  ],
  templateUrl: './app.component.html',
  styleUrl: './app.component.css'
})
export class AppComponent implements OnInit {
  constructor(private primengConfig: PrimeNG) {}

  ngOnInit() {
    setPtBrPrimeNgConfig(this.primengConfig);
  }
}
