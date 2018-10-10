---
title: TableDef.LastUpdated Property (DAO)
TOCTitle: LastUpdated Property
ms:assetid: fafe54e2-2cf0-5874-92b9-6e20a65e77ef
ms:mtpsurl: https://msdn.microsoft.com/library/Ff837164(v=office.15)
ms:contentKeyID: 48548859
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 3840ef8b2a01f28bd2a9881848c813f85411fb7b
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/09/2018
ms.locfileid: "25481837"
---
# <a name="tabledeflastupdated-property-dao"></a>TableDef.LastUpdated Property (DAO)


**Применимо к**: Access 2013 | Office 2013

Возвращает дату и время последнего изменения, внесенные в объект. Только для чтения **Variant**.

## <a name="syntax"></a>Синтаксис

*выражение* . LastUpdated

*выражение* Переменная, которая представляет собой объект- **TableDef** .

## <a name="remarks"></a>Замечания

**DateCreated** и **LastUpdated** возвращают дату и время создания или последнего обновления. В многопользовательской среде пользователи должны получить эти параметры непосредственно из файлового сервера, чтобы избежать несоответствия в DateCreated и параметры свойства LastUpdated.

