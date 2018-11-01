---
title: Свойство Rowset (ADO)
TOCTitle: Rowset property (ADO)
ms:assetid: 1a1cb3ef-8f3c-30c1-3eb0-8618fdcacd53
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248946(v=office.15)
ms:contentKeyID: 48543515
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 7be8abbce6828dd202e0c64eec342de9198f7a9b
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/31/2018
ms.locfileid: "25878537"
---
# <a name="rowset-property-ado"></a>Свойство Rowset (ADO)


**Применимо к**: Access 2013, Office 2013



Получает или задает объект OLE DB **строк** из/на объекте **ADORecordsetConstruction** . При использовании put\_включается набор строк, набор строк, в объект ADO **Recordset** .

Для чтения и записи.

## <a name="syntax"></a>Синтаксис

HRESULT get\_набор строк (\[out retval\] IUnknown\* \* ppRowset);

Поместите HRESULT\_набор строк (\[в\] IUnknown\* pRowset);

## <a name="parameters"></a>Параметры

  - *ppRowset*

  - Указатель на объект OLE DB **строк** .

  - *PRowset*

  - Объект OLE DB **строк** .

## <a name="return-values"></a>Возвращаемые значения

Этот метод свойство возвращает стандартных значений HRESULT, включая S\_ОК и E\_с ОШИБКОЙ.

## <a name="applies-to"></a>Применимо к

[ADORecordsetConstruction](adorecordsetconstruction-interface-ado.md)

