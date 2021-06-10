---
title: Свойство QueryDef.Updatable (DAO)
TOCTitle: Updatable Property
ms:assetid: 9b978b7d-1d76-ff27-a032-dd94660fb088
ms:mtpsurl: https://msdn.microsoft.com/library/Ff198056(v=office.15)
ms:contentKeyID: 48546575
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: c5321e834f1dd5ed663033cacb530962d7beeb5a
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32303334"
---
# <a name="querydefupdatable-property-dao"></a>Свойство QueryDef.Updatable (DAO)


**Область применения**: Access 2013, Office 2013

Возвращает значение, которое указывает на то, можно ли изменить DAO объект. Только для чтения, **Boolean**.

## <a name="syntax"></a>Синтаксис

*выражения* . Updatable

*выражение*: переменная, представляющая объект **QueryDef**.

## <a name="remarks"></a>Примечания

Свойство **Updatable** объекта **QueryDef** задалось true, если определение запроса может быть обновлено, даже если в результате объект **[Recordset](recordset-object-dao.md)** не является updatable. 

