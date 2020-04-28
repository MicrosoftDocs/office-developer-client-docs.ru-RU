---
title: Свойство Row — объекты данных ActiveX (ADO)
TOCTitle: Row property (ADO)
ms:assetid: 1c2b0e27-7232-4b1c-826c-9dc15d758851
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248959(v=office.15)
ms:contentKeyID: 48543562
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 9b4beaa742bfc46ecd32fc04733c3e6ddaf12aa2
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32306484"
---
# <a name="row-property-ado"></a>Свойство Row (ADO)

**Область применения**: Access 2013, Office 2013

Получает или задает объект **строки** OLE DB from/On объекта **ADORecordConstruction** . При использовании **строки PUT\_** для установки объекта **Row** строка будет преобразована в объект **записи** ADO. Для чтения и записи.

## <a name="syntax"></a>Синтаксис

HRESULT Get\_Row (\[out,\] IUnknown IUnknown\* \* ппров);

Строка размещения\_HRESULT (\[в\] интерфейсе IUnknown\* пров);

## <a name="parameters"></a>Параметры

|Параметр|Описание|
|:--------|:----------|
|*ппров* |Указатель на объект **строки** OLE DB.|
|*пров* |Объект **строки** OLE DB.|

## <a name="return-values"></a>Возвращаемые значения

Этот метод свойства возвращает стандартные значения HRESULT, включая S\_ОК и электронную\_ошибку.

## <a name="applies-to"></a>Сфера применения

[ADORecordConstruction](adorecordconstruction-interface-ado.md)

