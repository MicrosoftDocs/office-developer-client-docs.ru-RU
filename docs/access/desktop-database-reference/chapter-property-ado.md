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
 
Получает или задает объект OLE DB **Chapter** из/на **объект ADORecordsetConstruction.** При использовании **put \_ Chapter** для набора объекта **Chapter** подмножество строк превращается в объект ADO **Recordset.** Это задает текущую главу объекта **Rowset.** Для чтения и записи.

## <a name="syntax"></a>Синтаксис

HRESULT \_ get Chapter \[ (out, retval \] long \* plChapter);

HRESULT \_ put Chapter \[ (in \] long lChapter);

## <a name="parameters"></a>Параметры

|Параметр|Описание|
|:--------|:----------|
|*plChapter* |Указатель на ручку главы.|
|*LChapter* |Ручка главы.|

## <a name="return-values"></a>Возвращаемые значения

Этот метод свойства возвращает стандартные значения HRESULT, в том числе S \_ OK и E \_ FAIL.

## <a name="applies-to"></a>Применимость

[ADORecordsetConstruction](adorecordsetconstruction-interface-ado.md)

