---
title: Свойство Error.Description (DAO)
TOCTitle: Description Property
ms:assetid: 47a84bec-3258-f2c7-e1af-239da39844dc
ms:mtpsurl: https://msdn.microsoft.com/library/Ff193218(v=office.15)
ms:contentKeyID: 48544601
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- dao360.chm1053358
f1_categories:
- Office.Version=v15
localization_priority: Normal
ms.openlocfilehash: 1d7e949771e764c22e93ef56059930ccf39584ab
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32293506"
---
# <a name="errordescription-property-dao"></a>Свойство Error.Description (DAO)


**Область применения**: Access 2013, Office 2013
 

Возвращает описательную строку, связанную с ошибкой. Это свойство по умолчанию для объекта **Error.**

## <a name="syntax"></a>Синтаксис

*выражение .* Описание

*выражение* Переменная, представляюная объект **Error.**

## <a name="remarks"></a>Заметки

Свойство **Description** содержит краткое описание ошибки. Это свойство используется для оповещения пользователя об ошибке, которую невозможно или не нужно обрабатывать.

## <a name="example"></a>Пример

В этом примере показана привратная ошибка, ее ловка и отображение свойств **Description,** **Number,** **Source,** **HelpContext** и **HelpFile** итоговых объектов Error.

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

