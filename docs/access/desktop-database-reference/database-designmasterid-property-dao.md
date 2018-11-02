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
ms.openlocfilehash: 1d15cc036b33e2b64f54b89f4f8ed5c69d9fdcbe
ms.sourcegitcommit: d7248f803002b31cf7fc561b03530199a9b0a8fd
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/02/2018
ms.locfileid: "25930492"
---
# <a name="databasedesignmasterid-property-dao"></a>Свойство Database.DesignMasterID (DAO)

**Применимо к**: Access 2013, Office 2013

Задает или возвращает 16-битное значение, уникальным образом идентифицирующее репликой в наборе реплик (только для рабочих областей Microsoft Access).

## <a name="syntax"></a>Синтаксис

*выражение* . DesignMasterID

*выражение* Переменная, которая представляет собой объект **базы данных** .

## <a name="remarks"></a>Примечания

Свойство **DesignMasterID** следует устанавливать только в том случае, если необходимо перенести текущей основной. Установка для этого свойства выполняет определенные в реплике набора реплик основной.

> [!NOTE]
> Никогда не создавать второй репликой в наборе реплик. Наличие из второго основной реплике может привести к потере данных.

Чрезмерную обстоятельствах — например, если основной удалены или повреждены — это свойство можно задать в текущей реплики. Тем не менее Установка этого свойства реплики при наборе уже существует другой реплике может разделы наборе на два набора несовместимые и предотвратить дальнейшая синхронизация данных.

Если вы решили создать новый основной набор реплику, синхронизируйте его с все реплики в наборе перед установкой **DesignMasterID** в реплике репликации. Чтобы сделать его основной реплики необходимо открыть в монопольном режиме.

При внесении реплики, предназначенная только для чтения в основной, реплики конечного выполняется чтение и запись; старый основной также остается чтения и записи.

Настройка свойства **DesignMasterID** хранится в таблице MSysRepInfo системы.

## <a name="example"></a>Пример

В этом примере присваивает свойству **DesignMasterID** значение свойства **ReplicaID** Установка другой базы данных, что делает репликой в наборе реплик базы данных. Образцы оформления старой и новой синхронизированы для обновления изменения. Для работы этого кода необходимо создать основной реплики и реплики, включают их имена и пути к соответствующим образом и запуска этого кода из отличный от старой и новой основной базы данных.

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

