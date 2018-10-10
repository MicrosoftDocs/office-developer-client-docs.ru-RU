---
title: onReadyStateChange Event (RDS)
TOCTitle: onReadyStateChange Event (RDS)
ms:assetid: 88102ee5-cca9-8ccb-5aca-55cda71abc4d
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249593(v=office.15)
ms:contentKeyID: 48546126
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: dec783aaa76745b73bd031b00f1b8587a58eb165
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/09/2018
ms.locfileid: "25481953"
---
# <a name="onreadystatechange-event-rds"></a>onReadyStateChange Event (RDS)


**Применимо к**: Access 2013 | Office 2013


Событие **onReadyStateChange** вызывается каждый раз, когда изменяется значение свойства [ReadyState](readystate-property-rds.md) .

## <a name="syntax"></a>Синтаксис

onReadyStateChange

## <a name="parameters"></a>Параметры

Нет.

## <a name="remarks"></a>Замечания

Свойство **ReadyState** отражает ход выполнения [RDS. DataControl](datacontrol-object-rds.md) как асинхронно получает данные в его объекта [набора записей](recordset-object-ado.md) . Событие **onReadyStateChange** используется для отслеживания изменений в свойстве **ReadyState** каждый раз, когда они возникают. Это эффективнее, чем периодически проверки значения свойства.

