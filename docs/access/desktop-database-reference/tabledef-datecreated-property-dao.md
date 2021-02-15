---
title: Свойство TableDef.DateCreated (DAO)
TOCTitle: DateCreated Property
ms:assetid: fedd28e9-41a4-db7f-9ba9-6ada350d594a
ms:mtpsurl: https://msdn.microsoft.com/library/Ff837292(v=office.15)
ms:contentKeyID: 48548947
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: a5dc326b271e8444211bba0cd2d3c37c047ac205
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32314541"
---
# <a name="tabledefdatecreated-property-dao"></a>Свойство TableDef.DateCreated (DAO)


**Область применения**: Access 2013, Office 2013

Возвращает дату и время создания объекта (только для рабочей области Microsoft Access). Только для чтения, **Variant**.

## <a name="syntax"></a>Синтаксис

*выражение .* DateCreated

*выражение*: переменная, представляющая объект **TableDef**.

## <a name="remarks"></a>Комментарии

**DateCreated** и **LastUpdated** возвращают дату и время создания или последнего обновления объекта. В многомерной среде пользователи должны получить эти параметры непосредственно с файлового сервера, чтобы избежать несоответствий в параметрах свойств DateCreated и LastUpdated.

