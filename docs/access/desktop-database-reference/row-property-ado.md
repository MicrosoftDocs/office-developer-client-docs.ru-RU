---
title: Строка свойство - ActiveX Data Objects (ADO)
TOCTitle: Row property (ADO)
ms:assetid: 1c2b0e27-7232-4b1c-826c-9dc15d758851
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248959(v=office.15)
ms:contentKeyID: 48543562
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 1882486de2a2dfe61b98d4461abeea9cbcc23363
ms.sourcegitcommit: 980a96cf444882d3d34cecb5faac8f8a7b7c4b57
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/03/2018
ms.locfileid: "25949315"
---
# <a name="row-property-ado"></a>Свойство Row (ADO)

**Применимо к**: Access 2013, Office 2013

Получает или задает объект OLE DB **строку** из/на объекте **ADORecordConstruction** . При использовании **поместить\_строки** Чтобы установить для объекта **строки** , строка включается в объект ADO **записи** . Для чтения и записи.

## <a name="syntax"></a>Синтаксис

HRESULT get\_строки (\[out retval\] IUnknown\* \* ppRow);

Поместите HRESULT\_строки (\[в\] IUnknown\* pRow);

## <a name="parameters"></a>Параметры

|Параметр|Описание|
|:--------|:----------|
|*ppRow* |Указатель на объект OLE DB **строки** .|
|*PRow* |Объект OLE DB **строки** .|

## <a name="return-values"></a>Возвращаемые значения

Этот метод свойство возвращает стандартных значений HRESULT, включая S\_ОК и E\_с ОШИБКОЙ.

## <a name="applies-to"></a>Область применения

[ADORecordConstruction](adorecordconstruction-interface-ado.md)

