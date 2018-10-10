---
title: Rowset Property (ADO)
TOCTitle: Rowset Property (ADO)
ms:assetid: 1a1cb3ef-8f3c-30c1-3eb0-8618fdcacd53
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248946(v=office.15)
ms:contentKeyID: 48543515
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 95a33fb3d24e5cdbf608d268781be0dd536fa315
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/09/2018
ms.locfileid: "25481481"
---
# <a name="rowset-property-ado"></a>Rowset Property (ADO)


**Применимо к**: Access 2013 | Office 2013



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

## <a name="return-values"></a>Return Values

Этот метод свойство возвращает стандартных значений HRESULT, включая S\_ОК и E\_с ОШИБКОЙ.

## <a name="applies-to"></a>Применимо к

[ADORecordsetConstruction](adorecordsetconstruction-interface-ado.md)

