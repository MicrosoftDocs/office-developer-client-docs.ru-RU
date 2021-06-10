---
title: Свойство QueryDef.LastUpdated (DAO)
TOCTitle: LastUpdated Property
ms:assetid: 3b7818d4-054e-54e2-bf63-58b340bb4a90
ms:mtpsurl: https://msdn.microsoft.com/library/Ff192665(v=office.15)
ms:contentKeyID: 48544287
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 1876e92381828075edca3bbfcbae63e706a21365
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32303313"
---
# <a name="querydeflastupdated-property-dao"></a>Свойство QueryDef.LastUpdated (DAO)


**Область применения**: Access 2013, Office 2013

Возвращает дату и время последнего изменения, выполненного в объекте. Только для чтения, **Variant**.

## <a name="syntax"></a>Синтаксис

*выражения* . LastUpdated

*выражение*: переменная, представляющая объект **QueryDef**.

## <a name="remarks"></a>Примечания

**DateCreated** и **LastUpdated** возвращают дату и время создания или последнего обновления объекта. В многоуровневой среде пользователи должны получать эти параметры непосредственно с файлового сервера, чтобы избежать расхождений в параметрах свойств DateCreated и LastUpdated.

