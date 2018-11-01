---
title: onReadyStateChange событий (RDS)
TOCTitle: onReadyStateChange Event (RDS)
ms:assetid: 88102ee5-cca9-8ccb-5aca-55cda71abc4d
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249593(v=office.15)
ms:contentKeyID: 48546126
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 7bea7d7ae5a7fe0681af315c8569bf9b67d8bd82
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/31/2018
ms.locfileid: "25869234"
---
# <a name="onreadystatechange-event-rds"></a>onReadyStateChange событий (RDS)


**Применимо к**: Access 2013, Office 2013


Событие **onReadyStateChange** вызывается каждый раз, когда изменяется значение свойства [ReadyState](readystate-property-rds.md) .

## <a name="syntax"></a>Синтаксис

onReadyStateChange

## <a name="parameters"></a>Параметры

Нет.

## <a name="remarks"></a>Замечания

Свойство **ReadyState** отражает ход выполнения [RDS. DataControl](datacontrol-object-rds.md) как асинхронно получает данные в его объекта [набора записей](recordset-object-ado.md) . Событие **onReadyStateChange** используется для отслеживания изменений в свойстве **ReadyState** каждый раз, когда они возникают. Это эффективнее, чем периодически проверки значения свойства.

