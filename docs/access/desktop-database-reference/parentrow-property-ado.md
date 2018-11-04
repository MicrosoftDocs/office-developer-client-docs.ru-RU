---
title: Свойство ParentRow (ADO)
TOCTitle: ParentRow property (ADO)
ms:assetid: c7520353-9428-9c8f-9d21-ff42e30e1193
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249971(v=office.15)
ms:contentKeyID: 48547638
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 06bb1110dfa7e7a055fa6cd863dcd2cc17f3f585
ms.sourcegitcommit: 980a96cf444882d3d34cecb5faac8f8a7b7c4b57
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/03/2018
ms.locfileid: "25950154"
---
# <a name="parentrow-property-ado"></a>Свойство ParentRow (ADO)

**Применимо к**: Access 2013, Office 2013

Задает объект **ADORecordConstruction** контейнер объекта OLE DB **строку** , чтобы родительской строки включается в объект ADO **записи** .

Только для записи.

## <a name="syntax"></a>Синтаксис

Поместите HRESULT\_ParentRow (\[в\] IUnknown\* pParent);

## <a name="parameters"></a>Параметры

|Параметр|Описание|
|:--------|:----------|
|*pParent* |Контейнер для строки.|

## <a name="return-values"></a>Возвращаемые значения

Этот метод свойство возвращает стандартных значений HRESULT, включая S\_ОК и E\_с ОШИБКОЙ.

## <a name="applies-to"></a>Область применения

[ADORecordConstruction](adorecordconstruction-interface-ado.md)

