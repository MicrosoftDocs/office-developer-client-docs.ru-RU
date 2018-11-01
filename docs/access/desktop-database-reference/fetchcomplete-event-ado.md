---
title: Событие FetchComplete (ADO)
TOCTitle: FetchComplete Event (ADO)
ms:assetid: 4863d5b5-7d77-bdef-c511-f85c9e6dec9d
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249224(v=office.15)
ms:contentKeyID: 48544621
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: e4b72bb3e05b4ef05358a80faffaa0ee4ce08a80
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/31/2018
ms.locfileid: "25882401"
---
# <a name="fetchcomplete-event-ado"></a>Событие FetchComplete (ADO)


**Применимо к**: Access 2013, Office 2013


Событие **FetchComplete** вызывается после извлечения всех записей в объемных асинхронной операции в [набора записей](recordset-object-ado.md).

## <a name="syntax"></a>Синтаксис

FetchComplete*pError*, *adStatus* *pRecordset*

## <a name="parameters"></a>Параметры

  - *pError*

  - Объект [Error](error-object-ado.md) . Описание ошибки, возникшей при имеет значение **adStatus** **adStatusErrorsOccurred**; в противном случае он не задан.

  - *adStatus*

  - [EventStatusEnum](eventstatusenum.md)
    
    Прежде чем возвращает это событие, присвойте этому параметру значение **adStatusUnwantedEvent** , чтобы запретить последующие уведомления.

  - *pRecordset*

  - Объект **набора записей** . Объект, для которого возвращенных записей.

## <a name="remarks"></a>Замечания

Чтобы использовать **FetchComplete** с помощью Microsoft Visual Basic, необходим Visual Basic 6.0 или более поздней версии.

