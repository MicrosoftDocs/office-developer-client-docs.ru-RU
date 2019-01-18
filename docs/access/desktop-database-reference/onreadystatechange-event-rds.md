---
title: Событие onReadyStateChange (RDS)
TOCTitle: onReadyStateChange event (RDS)
ms:assetid: 88102ee5-cca9-8ccb-5aca-55cda71abc4d
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249593(v=office.15)
ms:contentKeyID: 48546126
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: ec2104634d9158d59d488b50d543cf0e57d9bd62
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/17/2019
ms.locfileid: "28699732"
---
# <a name="onreadystatechange-event-rds"></a>Событие onReadyStateChange (RDS)

**Применимо к**: Access 2013, Office 2013

Событие **onReadyStateChange** вызывается каждый раз, когда изменяется значение свойства [ReadyState](readystate-property-rds.md) .

## <a name="syntax"></a>Синтаксис

onReadyStateChange

## <a name="parameters"></a>Параметры

Нет.

## <a name="remarks"></a>Замечания

Свойство **ReadyState** отражает ход выполнения [RDS. DataControl](datacontrol-object-rds.md) как асинхронно получает данные в его объекта [набора записей](recordset-object-ado.md) . Событие **onReadyStateChange** используется для отслеживания изменений в свойстве **ReadyState** каждый раз, когда они возникают. Это эффективнее, чем периодически проверки значения свойства.

