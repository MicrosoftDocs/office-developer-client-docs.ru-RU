---
title: 'Step 5: DataControl is Made Usable (RDS Tutorial)'
TOCTitle: 'Step 5: DataControl is Made Usable (RDS Tutorial)'
ms:assetid: 9eff5732-2743-6891-dfa6-0991645e17ad
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249728(v=office.15)
ms:contentKeyID: 48546672
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 1d9bd24d0aff1134a6af77862fd8f011d4ddff9f
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/09/2018
ms.locfileid: "25482537"
---
# <a name="step-5-datacontrol-is-made-usable-rds-tutorial"></a>Step 5: DataControl is Made Usable (RDS Tutorial)


**Применимо к**: Access 2013 | Office 2013

Возвращаемый объект **набора записей** доступна для использования. Можно проверить, перейдите или измените его так, как и любой другой **набора записей**. Что можно сделать с помощью **набора записей** зависит от среды. Visual Basic и Visual C++ имеют визуальные элементы управления, которые могут использовать **записей** прямо или косвенно с помощью Включение управления данными.

Например при отображении веб-страницы в Microsoft Internet Explorer, может потребоваться отображение данных объекта **набора записей** в элементе управления visual. Визуальные элементы управления на веб-странице не может получить доступ к объекта **набора записей** напрямую. Тем не менее они могут доступ к объекту **набора записей** с [RDS. DataControl](datacontrol-object-rds.md). **RDS. DataControl** становится могут использоваться с помощью визуального элемента управления, если свойство [SourceRecordset](recordset-sourcerecordset-properties-rds.md) имеет значение в объект **набора записей** .

Элемент управления visual объект должен иметь значение **RDS. параметра **DATASRC** DataControl**и его свойства **DATAFLD** поля объекта **набора записей** (столбца).

В этом руководстве задайте для свойства **SourceRecordset** :

```vb 
 
Sub RDSTutorial5() 
 Dim DS as New RDS.DataSpace 
 Dim RS as ADODB.Recordset 
 Dim DC as New RDS.DataControl 
 Dim DF as Object 
 Set DF = DS.CreateObject("RDSServer.DataFactory", "https://yourServer") 
 Set RS = DF.Query ("DSN=Pubs", "SELECT * FROM Authors") 
 DC.SourceRecordset = RS ' Visual controls can now bind to DC. 
... 
```
