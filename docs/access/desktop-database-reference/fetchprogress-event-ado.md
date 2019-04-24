---
title: Событие событие fetchprogress (ADO)
TOCTitle: FetchProgress event (ADO)
ms:assetid: 09145d9a-ea5e-b41c-6c54-33ec83e642a9
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248828(v=office.15)
ms:contentKeyID: 48543114
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: d863f51e7836acdc577ecd720df77114ed66f067
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32293184"
---
# <a name="fetchprogress-event-ado"></a>Событие событие fetchprogress (ADO)

**Область применения**: Access 2013, Office 2013

Событие **событие fetchprogress** вызывается периодически в течение длительной асинхронной операции, чтобы сообщить, сколько строк в данный момент было извлечено в [набор записей](recordset-object-ado.md).

## <a name="syntax"></a>Синтаксис

*Ход выполнения*событие fetchprogress, *макспрогресс*, *адстатус*, пред **

## <a name="parameters"></a>Параметры

|Параметр|Описание|
|:--------|:----------|
|*Progress* |**Длинное** значение, указывающее количество записей, которые в настоящее время были получены операцией выборки.|
|*Макспрогресс* |**Длинное** значение, указывающее максимальное количество получаемых записей.|
|*Адстатус* |Значение состояния [евентстатусенум](eventstatusenum.md) .|
|*предшнур* |Объект **Recordset** , представляющий собой объект, для которого извлекаются записи.|

## <a name="remarks"></a>Замечания

При использовании **событие fetchprogress** с дочернИм объектом **Recordset**имейте в виду, что значения параметров *Progress* и *макспрогресс* являются производными от базового набора строк [службы курсора](microsoft-cursor-service-for-ole-db-ado-service-component.md) . Возвращаемые значения представляют общее число записей в базовом наборе строк, а не только число записей в текущей главе.

> [!NOTE]
> Чтобы использовать **событие fetchprogress** с Microsoft Visual Basic, требуется Visual Basic 6,0 или более поздней версии.


