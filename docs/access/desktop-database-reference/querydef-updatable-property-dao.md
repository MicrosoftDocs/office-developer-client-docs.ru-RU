---
title: QueryDef.Updatable Property (DAO)
TOCTitle: Updatable Property
ms:assetid: 9b978b7d-1d76-ff27-a032-dd94660fb088
ms:mtpsurl: https://msdn.microsoft.com/library/Ff198056(v=office.15)
ms:contentKeyID: 48546575
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 6ca30e86bd61bc5459a552423bd451c7b158996d
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/09/2018
ms.locfileid: "25480041"
---
# <a name="querydefupdatable-property-dao"></a>QueryDef.Updatable Property (DAO)


**Применимо к**: Access 2013 | Office 2013

Возвращает значение, указывающее, является ли объект DAO можно изменить. Только для чтения, **Boolean**.

## <a name="syntax"></a>Синтаксис

*выражение* . Обновляемые

*выражение* Переменная, которая представляет собой объект- **QueryDef** .

## <a name="remarks"></a>Замечания

Свойство **с возможностью записи** объекта **QueryDef** имеет значение **True** , если определение запроса могут быть обновлены, даже в том случае, если не обновляемый объекте результирующего **[набора записей](recordset-object-dao.md)** .

