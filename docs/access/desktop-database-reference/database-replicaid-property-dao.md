---
title: Свойство Database.ReplicaID (DAO)
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
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/17/2019
ms.locfileid: "28703932"
---
# <a name="databasereplicaid-property-dao"></a>Свойство Database.ReplicaID (DAO)


**Применимо к**: Access 2013, Office 2013


Возвращает 16-битное значение, уникальным образом идентифицирующее реплики базы данных (только для рабочих областей Microsoft Access).

## <a name="syntax"></a>Синтаксис

*выражение* . ReplicaID

*выражение* Переменная, которая представляет собой объект **базы данных** .

## <a name="remarks"></a>Замечания

Возвращаемое значение — это значение **GUID** , который уникальным образом определяет, так и основной.

Ядро базы данных Microsoft Access автоматически создает это значение при создании новой реплики.

Свойство **ReplicaID** каждой реплики (и основной) хранятся в таблице MSysReplicas системы.

## <a name="example"></a>Пример

В этом примере вносятся реплики из основной части Northwind.mdb и возвращает реплики **ReplicaID**, которая создается автоматически ядром СУБД Microsoft Access. (Если основной Northwind еще не создан, ссылка на свойство **является реплицируемым** или измените имя базы данных в коде для имеющегося образца разработки).

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

