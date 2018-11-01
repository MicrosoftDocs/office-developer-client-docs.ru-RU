---
title: Error.Source Property (DAO)
TOCTitle: Source Property
ms:assetid: 3c101cac-278e-025e-55a4-8a9d1ee7db3c
ms:mtpsurl: https://msdn.microsoft.com/library/Ff192677(v=office.15)
ms:contentKeyID: 48544302
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- dao360.chm1053360
f1_categories:
- Office.Version=v15
ms.openlocfilehash: 16d043f1906744988af35708a954e9224256f8f7
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/31/2018
ms.locfileid: "25867995"
---
# <a name="errorsource-property-dao"></a>Error.Source Property (DAO)


**Применимо к**: Access 2013, Office 2013


Возвращает имя объекта или приложения, вызвавшего ошибку.

## <a name="syntax"></a>Синтаксис

*выражение* . Источник

*выражение* Переменная, которая содержит объект **Error** .

## <a name="remarks"></a>Замечания

Значение свойства **источника** обычно является именем класса объекта или программный идентификатор. Используйте свойство **Source** для предоставления пользователям со сведениями, если код не может обработать ошибку, созданную в объект в другом приложении.

Например если доступ к Microsoft Excel, и возникает ошибка «Деление на ноль», Microsoft Excel показана **Error.Number** в код Microsoft Excel для этой ошибки и свойство **Source** на Excel.Application. Обратите внимание на то, что, если ошибка возникает в другой объект с именем с Microsoft Excel, Microsoft Excel перехватывает ошибку и по-прежнему задает **Error.Number** код Microsoft Excel. Тем не менее другие **ошибки** объекта свойства (в том числе **источника**) будет сохранять значения как набор объектом, вызвавшей ошибку. Свойство **Source** всегда содержит имя объекта, вызвавшего ошибку.

На основе всей документацию ошибок, можно написать код, который будет обрабатывать ошибки соответствующим образом. Если обработчик ошибок не удается, можно использовать объект сведения **[об ошибке](error-object-dao.md)** для описания для пользователя, с помощью свойства **источника** и другие свойства **об ошибках** для предоставления пользователю информации о какой объект изначально, возникающие ошибки Ошибка, описание ошибки и т. д.


> [!NOTE]
> Конструкция **On Error Resume Next** может оказаться предпочтительнее **On Error GoTo** при работе с ошибки, возникающие во время доступа к другим объектам. Проверка свойства объекта **ошибки** после каждого взаимодействия с объектом устраняет неопределенность, о которых объект кода доступ к при возникновении ошибки. Таким образом вам может быть том, какой объект поместил код ошибки в **Error.Number**, а также какой объект изначально создал ошибку (**Error.Source**).

## <a name="example"></a>Пример

В этом примере принудительно ошибку, его перехватывает и отображает свойства **Description**, **номер**, **источник**, **HelpContext**и **HelpFile** итоговый объект **Error** .

```vb
    Sub DescriptionX() 
     
     Dim dbsTest As Database 
     
     On Error GoTo ErrorHandler 
     
     ' Intentionally trigger an error. 
     Set dbsTest = OpenDatabase("NoDatabase") 
     
     Exit Sub 
     
    ErrorHandler: 
     Dim strError As String 
     Dim errLoop As Error 
     
     ' Enumerate Errors collection and display properties of 
     ' each Error object. 
     For Each errLoop In Errors 
     With errLoop 
     strError = _ 
     "Error #" & .Number & vbCr 
     strError = strError & _ 
     " " & .Description & vbCr 
     strError = strError & _ 
     " (Source: " & .Source & ")" & vbCr 
     strError = strError & _ 
     "Press F1 to see topic " & .HelpContext & vbCr 
     strError = strError & _ 
     " in the file " & .HelpFile & "." 
     End With 
     MsgBox strError 
     Next 
     
     Resume Next 
     
    End Sub
```
