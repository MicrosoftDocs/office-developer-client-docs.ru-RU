---
title: Свойство Chapter (ADO)
TOCTitle: Chapter property (ADO)
ms:assetid: d7c9478e-487f-7023-1dd8-5313433dbc5e
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250085(v=office.15)
ms:contentKeyID: 48548014
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: b4f4efc2ffab9f7996b2d805658b985badbaf87e
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32296397"
---
# <a name="chapter-property-ado"></a>Свойство Chapter (ADO)

**Область применения**: Access 2013, Office 2013
 
Получает или задает объект главы OLE DB **из/объекта** **ADORecordsetConstruction.** При использовании **put \_ Chapter** для применения объекта **Chapter** подмножество строк превращается в объект ADO **Recordset.** Это задает текущую главу объекта **Rowset.** Для чтения и записи.

## <a name="syntax"></a>Синтаксис

HRESULT get \_ Chapter( \[ out, retval \] long \* plChapter);

HRESULT put \_ Chapter( \[ in long \] lChapter);

## <a name="parameters"></a>Параметры

|Параметр|Описание|
|:--------|:----------|
|*plChapter* |Указатель на ладную часть главы.|
|*LChapter* |Обработка главы.|

## <a name="return-values"></a>Возвращаемые значения

Этот метод свойства возвращает стандартные значения HRESULT, включая S \_ OK и E \_ FAIL.

## <a name="applies-to"></a>Применимость

[ADORecordsetConstruction](adorecordsetconstruction-interface-ado.md)

