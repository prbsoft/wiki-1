# Кнопка

## Чтобы открыть карточку\(cartela\) по нажатию кнопки и передать в нее параметр\(nrdoc\), необходимо в свойстве Params кнопки прописать: {#H42744243E43144B43E44243A44044B44244C43A43044044243E44743A44328cartela2943F43E43D43043643044243844E43A43D43E43F43A43843843F43544043543443044244C43243D43543543F43044043043C43544244028nrdoc292C43D43543E43144543E43443843C43E43244143243E439441442432435Params43A43D43E43F43A43843F44043E43F43844143044244C:}

TargetType=cartela

TargetSection=ATTR\_ORD\_ADD

nrdoc=\_nrdoc

MainTA=1

Таким образом, мы определяем, что по кнопке открывается карточка, имя секции которой = ATTR\_ORD\_ADD. Передаем в форму параметр nrdoc=\_nrdoc, значение которого берется из запроса для панели, на которой расположена кнопка.

## Чтобы открыть форму по нажатию кнопки, необходимо в свойстве Params кнопки прописать: {#H42744243E43144B43E44243A44044B44244C44443E44043C44343F43E43D43043643044243844E43A43D43E43F43A4382C43D43543E43144543E43443843C43E43244143243E439441442432435Params43A43D43E43F43A43843F44043E43F43844143044244C:}

TargetType=form

TargetSection=FRM\_IMP\_ORD\_ADD

Мы указываем, что по нажатию кнопки открывается форма с именем секции = FRM\_IMP\_ORD\_ADD

## Чтобы выполнить действие по нажатию кнопки, необходимо в свойстве Params кнопки прописать: {#H42744243E43144B43244B43F43E43B43D43844244C43443543944144243243843543F43E43D43043643044243844E43A43D43E43F43A4382C43D43543E43144543E43443843C43E43244143243E439441442432435Params43A43D43E43F43A43843F44043E43F43844143044244C:}

TargetType=doc.action

action\_id=1

Мы указываем, что по нажатию кнопки выполняется действие, которое имеет id=1

