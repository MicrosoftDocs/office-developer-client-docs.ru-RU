---
title: Этап 5. Предоставление доступа к объекту DataControl (руководство по RDS)
TOCTitle: 'Step 5: DataControl is Made Usable (RDS Tutorial)'
ms:assetid: 9eff5732-2743-6891-dfa6-0991645e17ad
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249728(v=office.15)
ms:contentKeyID: 48546672
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: e5871138f2b82770f49da2d5f9d4977443b0664e
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/31/2018
ms.locfileid: "25884046"
---
# <a name="step-5-datacontrol-is-made-usable-rds-tutorial"></a>Этап 5. Предоставление доступа к объекту DataControl (руководство по RDS)


**Применимо к**: Access 2013, Office 2013

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

