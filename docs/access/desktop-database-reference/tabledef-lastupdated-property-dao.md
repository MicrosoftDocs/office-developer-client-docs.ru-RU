---
title: Свойство TableDef. Ластупдатед (DAO)
TOCTitle: LastUpdated Property
ms:assetid: fafe54e2-2cf0-5874-92b9-6e20a65e77ef
ms:mtpsurl: https://msdn.microsoft.com/library/Ff837164(v=office.15)
ms:contentKeyID: 48548859
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 994543132fb5323566bd876da066419d0986bd91
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32308416"
---
# <a name="tabledeflastupdated-property-dao"></a>Свойство TableDef. Ластупдатед (DAO)


**Область применения**: Access 2013, Office 2013

Возвращает дату и время последнего изменения, внесенного в объект. Только для чтения, **Variant**.

## <a name="syntax"></a>Синтаксис

*Expression* . Ластупдатед

*выражение*: переменная, представляющая объект **TableDef**.

## <a name="remarks"></a>Комментарии

**DateCreated** и **ластупдатед** возвращают дату и время создания или последнего обновления объекта. В многопользовательской среде пользователи должны получить эти параметры непосредственно с файлового сервера, чтобы избежать расхождений в параметрах свойств DateCreated и Ластупдатед.

