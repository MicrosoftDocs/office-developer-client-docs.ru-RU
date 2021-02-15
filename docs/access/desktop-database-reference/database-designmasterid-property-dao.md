---
title: Свойство Database.DesignMasterID (DAO)
TOCTitle: DesignMasterID Property
ms:assetid: c0545561-d44f-5479-8ae0-e3955db91761
ms:mtpsurl: https://msdn.microsoft.com/library/Ff822824(v=office.15)
ms:contentKeyID: 48547508
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- dao360.chm1053417
f1_categories:
- Office.Version=v15
localization_priority: Normal
ms.openlocfilehash: a189d16880fccdc34c169aee61c6781e1d86afa8
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32294934"
---
# <a name="databasedesignmasterid-property-dao"></a>Свойство Database.DesignMasterID (DAO)

**Область применения**: Access 2013, Office 2013

Задает или возвращает 16-byte-значение, которое уникальным образом идентифицирует master дизайна в наборе реплик (только для рабочей области Microsoft Access).

## <a name="syntax"></a>Синтаксис

*выражение .* DesignMasterID

*выражение*: переменная, представляющая объект **Database**.

## <a name="remarks"></a>Заметки

Свойство **DesignMasterID следует** устанавливать только в том случае, если необходимо переместить текущий объект Design Master. Установка этого свойства делает определенную реплику в реплике набором "Мастер проектирования".

> [!NOTE]
> Никогда не создавайте второй мастер проектирования в наборе реплик. Наличие второго мастера разработки может привести к потере данных.

В крайних обстоятельствах, например, если образец конструктора стирается или поврежден, можно установить это свойство в текущей реплике. Однако установка этого свойства в реплике, когда в наборе уже есть другой мастер разработки, может привести к разделению реплики на два неприсоедаемых набора и предотвратить дальнейшую синхронизацию данных.

Если вы решили сделать реплику новым хозяином дизайна для набора, синхронизируются со всеми репликами в наборе реплик, прежде чем устанавливать свойство **DesignMasterID** в реплике. Реплика должна быть открыта в монопольном режиме, чтобы сделать ее хозяином разработки.

Если вы сделаете реплику, предназначенную только для чтения, в мастере разработки, целевая реплика будет выполнена для чтения и записи; Старый мастер проектирования также остается для чтения и записи.

Параметр **свойства DesignMasterID** хранится в системной таблице MSysRepInfo.

## <a name="example"></a>Пример

В этом примере **свойству DesignMasterID** задан параметр **свойства ReplicaID** другой базы данных, что делает эту базу данных образцом разработки в наборе реплик. Старые и новые мастера проектирования синхронизируются для обновления изменений дизайна. Чтобы этот код работал, необходимо создать мастер проектирования и реплику, включить соответствующие имена и пути, а затем запустить этот код из базы данных, которая не является старой или новой.

```vb 
 Sub SetNewDesignMaster(strOldDM as String, _ 
    strNewDM as String) 
    
    Dim dbsOld As Database 
    Dim dbsNew As Database 
    
    ' Open the current Design Master in exclusive mode. 
    Set dbsOld = OpenDatabase(strOldDM, True) 
    
    ' Open the database that will become the new 
    ' Design Master. 
    Set dbsNew = OpenDatabase(strNewDM) 
    
    ' Make the new database the Design Master. 
    dbsOld.DesignMasterID = dbsNew.ReplicaID 
    
    ' Synchronize the old Design Master with the new 
    ' Design Master, and allow two-way exchanges. 
    dbsOld.Synchronize strNewDM, dbRepImpExpChanges 
    dbsOld.Close 
    dbsNew.Close 
 
 End Sub 
 
```

