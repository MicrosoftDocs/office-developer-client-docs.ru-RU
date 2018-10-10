---
title: SetProperty Macro Action
TOCTitle: SetProperty Macro Action
ms:assetid: 58d2eac3-35b2-e9f8-47e0-62c9b52f2c24
ms:mtpsurl: https://msdn.microsoft.com/library/Ff194340(v=office.15)
ms:contentKeyID: 48545004
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- vbaac10.chm139044
f1_categories:
- Office.Version=v15
ms.openlocfilehash: 6d7aa1deb4bea90e8319cccc763a4e087dd53ef0
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/09/2018
ms.locfileid: "25482576"
---
# <a name="setproperty-macro-action"></a>SetProperty Macro Action

**Применимо к**: Access 2013 | Office 2013

Действия **SetProperty** можно использовать для задания свойства для элемента управления в форму или отчет.

## <a name="setting"></a>Параметр

Действия **SetProperty** имеет следующие аргументы.

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Аргумент макрокоманды</p></th>
<th><p>Описание</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>Контрольное имя</p></td>
<td><p>Введите имя в поле или элемент управления, для которого требуется задать значение свойства. Используйте только имя элемента управления, но не полный синтаксис. Оставьте данный аргумент пустым, чтобы задать свойства для текущей формы или отчета.</p></td>
</tr>
<tr class="even">
<td><p>Свойство</p></td>
<td><p>Выберите свойство, которое требуется установить. <strong>В этой статье представлен список свойств, которые можно настроить с помощью этого действия см.</strong></p></td>
</tr>
<tr class="odd">
<td><p>Значение</p></td>
<td><p>Введите значение, является ли данное свойство должно быть задано. Для свойства, значения которых являются Да или нет, используйте <strong>значение -1</strong> для Да и <strong>0</strong> для нет.</p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a>Замечания

- Действия **SetProperty** можно использовать для настройки следующих свойств элемента управления: **включено**, **Visible**, **блокируется**, **слева**, **в начало**, **Ширина**, **Высота**, **цвет текста**, **Цвет фона**, или **Заголовок**.

- При вводе недопустимое значение аргумента ***значение*** ошибок нет, но доступа могут изменить свойство разные значения, в зависимости от того, как оно интерпретирует аргумент.

- Действие **SetProperty** в изолированном макрос можно использовать только в том случае, если вы поставьте перед ним действие, которое выбирает форму или отчет, содержащий элемент управления, для которого задаются свойства. Если форма или отчет не открыт, можно использовать действие **ОткрытьФорму** или **ОткрытьОтчет** открыть и затем выберите ее. Если форма или отчет уже открыт, чтобы выбрать его можно использовать **ВыделитьОбъект** . Затем можно использовать действие **SetProperty** для свойства. Выберите объект не является обязательным, если вы используете действие **SetProperty** в макросе, который встроен в элемент управления на одну форму или отчет в качестве элемента управления, для которого задаются свойства.

- Чтобы выполнить действия **SetProperty** в модуле VBA, используйте метод **SetProperty** **объекта** .

## <a name="example"></a>Пример

Следующий пример демонстрирует действие SetProperty используется для включения и отключения видимости **MyTextBox** текстовое поле.

**Пример кода предоставлен** [Справочник программиста Microsoft Access 2010](https://www.amazon.com/Microsoft-Access-2010-Programmers-Reference/dp/8126528125).

```vb
    Submacro: TestVisible
        SetProperty
            Control Name Text40
            Property Visible
            Value =Not[Text40].[Visible]
    End Submacro
```