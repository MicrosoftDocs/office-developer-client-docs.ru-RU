---
title: Свойство QueryDef. DateCreated (DAO)
TOCTitle: DateCreated Property
ms:assetid: f7585b34-8314-fb9f-daa6-cd1a8ad59d91
ms:mtpsurl: https://msdn.microsoft.com/library/Ff836910(v=office.15)
ms:contentKeyID: 48548763
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: a4a120eed6c20db73e1c23f31ea9329d00da2f0d
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32301073"
---
# <a name="querydefdatecreated-property-dao"></a>Свойство QueryDef. DateCreated (DAO)


**Область применения**: Access 2013, Office 2013

Возвращает дату и время создания объекта (только для рабочих областей Microsoft Access). Только для чтения, **Variant**.

## <a name="syntax"></a>Синтаксис

*Expression* . DateCreated

*выражение*: переменная, представляющая объект **QueryDef**.

## <a name="remarks"></a>Замечания

**DateCreated** и **ластупдатед** возвращают дату и время создания или последнего обновления объекта. В многопользовательской среде пользователи должны получить эти параметры непосредственно с файлового сервера, чтобы избежать расхождений в параметрах свойств DateCreated и Ластупдатед.

