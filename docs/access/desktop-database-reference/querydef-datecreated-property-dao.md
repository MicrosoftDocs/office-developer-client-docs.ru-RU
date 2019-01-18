---
title: Свойство QueryDef.DateCreated (DAO)
TOCTitle: DateCreated Property
ms:assetid: f7585b34-8314-fb9f-daa6-cd1a8ad59d91
ms:mtpsurl: https://msdn.microsoft.com/library/Ff836910(v=office.15)
ms:contentKeyID: 48548763
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: a4a120eed6c20db73e1c23f31ea9329d00da2f0d
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/17/2019
ms.locfileid: "28699683"
---
# <a name="querydefdatecreated-property-dao"></a>Свойство QueryDef.DateCreated (DAO)


**Применимо к**: Access 2013, Office 2013

Возвращает дату и время создания объекта (только для рабочих областей Microsoft Access). Только для чтения, **Variant**.

## <a name="syntax"></a>Синтаксис

*выражение* . DateCreated

*выражение* Переменная, которая представляет собой объект- **QueryDef** .

## <a name="remarks"></a>Замечания

**DateCreated** и **LastUpdated** возвращают дату и время создания или последнего обновления. В многопользовательской среде пользователи должны получить эти параметры непосредственно из файлового сервера, чтобы избежать несоответствия в DateCreated и параметры свойства LastUpdated.

