---
title: Свойство StayInSync (ADO)
TOCTitle: StayInSync property (ADO)
ms:assetid: 02c95c10-4032-14e1-e506-f334a8787142
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248792(v=office.15)
ms:contentKeyID: 48542966
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: bfc9ef5229fe230ad0c83ebde7a887e0fac0c233
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32308493"
---
# <a name="stayinsync-property-ado"></a>Свойство StayInSync (ADO)


**Область применения**: Access 2013, Office 2013

Указывает, изменяется ли ссылка на базовые дочерние записи (то есть глава) в иерархическом объекте ** [Recordset](recordset-object-ado.md) при изменении положения родительской строки.

## <a name="settings-and-return-values"></a>Параметры и возвращаемые значения

Задает или возвращает **логическое** значение. Значение по умолчанию — **True**. Если этот параметр **имеет значение true**, глава будет обновлена, если родительский объект **Recordset** изменяет положение строки; Если задано **значение false**, в главе будут содержаться ссылки на данные из предыдущей главы, несмотря на то, что родительский объект **Recordset** изменил положение строки.

## <a name="remarks"></a>Замечания

Это свойство применяется к иерархическим наборам записей, например, поддерживаемым [службой формирования данных (Майкрософт) для OLE DB](microsoft-data-shaping-service-for-ole-db-ado-service-provider.md), и должна быть задана для родительского объекта **Recordset** перед получением дочернего **набора записей** . Это свойство упрощает навигацию по иерархическим наборам записей.

