---
title: TableDef.DateCreated Property (DAO)
TOCTitle: DateCreated Property
ms:assetid: fedd28e9-41a4-db7f-9ba9-6ada350d594a
ms:mtpsurl: https://msdn.microsoft.com/library/Ff837292(v=office.15)
ms:contentKeyID: 48548947
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 6ffad5b1bee5756c969f03a920f453f1d3abf9e3
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/09/2018
ms.locfileid: "25480433"
---
# <a name="tabledefdatecreated-property-dao"></a>TableDef.DateCreated Property (DAO)


**Применимо к**: Access 2013 | Office 2013

Возвращает дату и время создания объекта (только для рабочих областей Microsoft Access). Только для чтения **Variant**.

## <a name="syntax"></a>Синтаксис

*выражение* . DateCreated

*выражение* Переменная, которая представляет собой объект- **TableDef** .

## <a name="remarks"></a>Замечания

**DateCreated** и **LastUpdated** возвращают дату и время создания или последнего обновления. В многопользовательской среде пользователи должны получить эти параметры непосредственно из файлового сервера, чтобы избежать несоответствия в DateCreated и параметры свойства LastUpdated.

