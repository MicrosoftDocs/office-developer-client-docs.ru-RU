---
title: События события connectcomplete и Disconnect (ADO)
TOCTitle: ConnectComplete and Disconnect events (ADO)
ms:assetid: 8ecb080b-7fc9-7565-25bd-bd57b983750d
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249629(v=office.15)
ms:contentKeyID: 48546293
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: e1e1d4487eb113c25e25ce6b9de051e33a4536b3
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32295991"
---
# <a name="connectcomplete-and-disconnect-events-ado"></a>События события connectcomplete и Disconnect (ADO)

**Область применения**: Access 2013, Office 2013

Событие **события connectcomplete** вызывается после *запуска*подключения. Событие **Disconnect** вызывается после *завершения*подключения.

## <a name="syntax"></a>Синтаксис

События connectcomplete*перрор*, *адстатус*, *пконнектион*

Отключение*адстатус*, *пконнектион*

## <a name="parameters"></a>Параметры

|Параметр|Описание|
|:--------|:----------|
|*Перрор* |Объект [Error](error-object-ado.md) . В нем описывается ошибка, которая возникла, если значение *адстатус* равно **адстатусеррорсоккурред**; в противном случае он не задается.|
|*Адстатус* |[Евентстатусенум](eventstatusenum.md). При вызове **события connectcomplete** этот параметр имеет значение **адстатусканцел** , если событие **событие willconnect** запросило отмену ожидающего подключения.<br/><br/>Перед возвращением любого события установите для этого параметра значение **адстатусунвантедевент** , чтобы предотвратить появление последующих уведомлений. Однако закрытие и повторное открытие [подключения](connection-object-ado.md) приводит к повторному возникновению этих событий.|
|*Пконнектион* |Объект **Connection** , к которому относится данное событие.|

