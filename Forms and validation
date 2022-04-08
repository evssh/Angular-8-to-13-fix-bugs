Exemple
___
8 Angular:
___
component.html
_
...
      <div
        *ngIf="form.get('email').invalid && form.get('email').touched"
        class="validation"
      >
        <small *ngIf="form.get('email').errors.required">
          Поле email не может быть пустым
        </small>

        <small *ngIf="form.get('email').errors.email">
          Введите корректный email
        </small>
      </div>
...
-
on Angular 13:
-
      <div
        *ngIf="form.get('email')?.invalid && form.get('email')?.touched"
        class="validation"
      >

        <small *ngIf="form.get('email')?.errors?.['required']"
        >Field not null</small>
        <small *ngIf="form.get('email')?.errors?.['email']"
        >Enter correct your email</small>
      </div>
-
component.ts
-
export class AppComponent implements OnInit {
  form: FormGroup

  ngOnInit() {
    this.form = new FormGroup({
      email: new FormControl('', [
        Validators.email,
        Validators.required
      ]),
      password: new FormControl(null, [
        Validators.required,
        Validators.minLength(6)
      ])
    })
  }

}
-
on Angular 13
_
export class AppComponent implements OnInit {
  form!: FormGroup

  ngOnInit() {
    this.form = new FormGroup({
      email: new FormControl('', [
        Validators.email,
        Validators.required
      ]),
      password: new FormControl(null, [
        Validators.required,
        Validators.minLength(6)
      ])
    })

  }


}
