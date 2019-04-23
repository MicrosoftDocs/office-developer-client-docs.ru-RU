---
title: событие Онреадистатечанже (RDS)
TOCTitle: onReadyStateChange event (RDS)
ms:assetid: 88102ee5-cca9-8ccb-5aca-55cda71abc4d
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249593(v=office.15)
ms:contentKeyID: 48546126
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: ec2104634d9158d59d488b50d543cf0e57d9bd62
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32288492"
---
# <a name="onreadystatechange-event-rds"></a>событие Онреадистатечанже (RDS)

**Область применения**: Access 2013, Office 2013

Событие **онреадистатечанже** вызывается всякий раз, когда изменяется значение свойства [ReadyState](readystate-property-rds.md) .

## <a name="syntax"></a>Синтаксис

Онреадистатечанже

## <a name="parameters"></a>Параметры

Нет.

## <a name="remarks"></a>Замечания

Свойство **ReadyState** отражает ход выполнения [RDS. Объект управления](datacontrol-object-rds.md) данными асинхронно извлекает данные в объект [Recordset](recordset-object-ado.md) . Используйте событие **онреадистатечанже** для отслеживания изменений в свойстве **ReadyState** , когда они происходят. Это более эффективно, чем периодическое извлечение значения свойства.

