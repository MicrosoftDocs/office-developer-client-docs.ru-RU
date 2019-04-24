---
title: Свойство Database. ReplicaID (DAO)
TOCTitle: ReplicaID Property
ms:assetid: cf2ca8a1-d13f-30e0-2ca1-dd32ac736c56
ms:mtpsurl: https://msdn.microsoft.com/library/Ff834672(v=office.15)
ms:contentKeyID: 48547805
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- dao360.chm1053375
f1_categories:
- Office.Version=v15
localization_priority: Normal
ms.openlocfilehash: 2ada9bf23a4b8fc34c5f9b4f24350fc6af91dc85
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32294717"
---
# <a name="databasereplicaid-property-dao"></a>Свойство Database. ReplicaID (DAO)


**Область применения**: Access 2013, Office 2013


Возвращает 16-байтовое значение, уникально идентифицирующее реплику базы данных (только для рабочих областей Microsoft Access).

## <a name="syntax"></a>Синтаксис

*Expression* . Одинаковые

*выражение*: переменная, представляющая объект **Database**.

## <a name="remarks"></a>Замечания

Возвращаемое значение — это значение **GUID** , которое уникально идентифицирует реплику или основную реплику.

Ядро СУБД Microsoft Access автоматически создает это значение при создании новой реплики.

Свойство **replicaId** каждой реплики (и основной реплики) хранится в системной таблице мсисрепликас.

## <a name="example"></a>Пример

В этом примере создается реплика из основной реплики базы данных Northwind. mdb, а затем возвращается значение **replicaId**реплики, которое автоматически создается ядром СУБД Microsoft Access. (Если вы еще не создали основную реплику базы данных, обратитесь к свойству **Реплицируемое** или измените имя базы данных в коде на существующую основную реплику.)

```vb 
Sub MakeReplicaReplicaIDX() 
 
 Dim dbsNorthwind As Database 
 Dim prpReplicaID As Property 
 Dim dbsReplica As Database 
 
 Set dbsNorthwind = OpenDatabase("Northwind.mdb") 
 
 ' Makes a new replica. 
 dbsNorthwind.MakeReplica "Nwreplica2.mdb", _ 
 "second replica" 
 dbsNorthwind.Close 
 
 ' Opens the new replica to read its ReplicaID. 
 Set dbsReplica = OpenDatabase("Nwreplica2.mdb") 
 
 Debug.Print dbsReplica.ReplicaID 
 dbsReplica.Close 
 
End Sub 
 
```

