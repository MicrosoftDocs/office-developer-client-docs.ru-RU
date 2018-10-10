---
title: FetchProgress Event (ADO)
TOCTitle: FetchProgress Event (ADO)
ms:assetid: 09145d9a-ea5e-b41c-6c54-33ec83e642a9
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248828(v=office.15)
ms:contentKeyID: 48543114
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 72a860ecd52e0481b55423f88e537eab3c8de2ae
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/09/2018
ms.locfileid: "25481508"
---
# <a name="fetchprogress-event-ado"></a>FetchProgress Event (ADO)


**Применимо к**: Access 2013 | Office 2013


Событие **FetchProgress** вызывается периодически во время длительных асинхронной операции для отчета, сколько увеличение количества строк в настоящее время извлечения в [набор записей](recordset-object-ado.md).

## <a name="syntax"></a>Синтаксис

FetchProgress*о ходе выполнения*, *MaxProgress* *adStatus*, *pRecordset*

## <a name="parameters"></a>Параметры

  - *Ход выполнения*

  - **Длинное** значение, указывающее количество записей, которые в настоящее время извлечения с операции выборки.

  - *MaxProgress*

  - Значение типа **Long** , указывающее максимальное число записей должен извлечь.

  - *adStatus*

  - Значение состояния [EventStatusEnum](eventstatusenum.md) .

  - *pRecordset*

  - Объект **набора записей** , — это объект, для которого извлекаются записи.

## <a name="remarks"></a>Замечания

При использовании **FetchProgress** с дочерним **записей**, обратите внимание, что значение параметра *хода выполнения* и *MaxProgress* являются производными от в базовом наборе строк [Службы курсора](microsoft-cursor-service-for-ole-db-ado-service-component.md) . Возвращаемые значения представляют общее число записей в базовом наборе строк, не только число записей в текущем.


> [!NOTE]
> <P>Чтобы использовать <STRONG>FetchProgress</STRONG> с помощью Microsoft Visual Basic, необходим Visual Basic 6.0 или более поздней версии.</P>


