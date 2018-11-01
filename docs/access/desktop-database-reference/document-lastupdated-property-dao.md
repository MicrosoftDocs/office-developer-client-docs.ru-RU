---
title: Document.LastUpdated Property (DAO)
TOCTitle: LastUpdated Property
ms:assetid: 9307ceee-095f-0364-fd5b-905bc523b9c0
ms:mtpsurl: https://msdn.microsoft.com/library/Ff197661(v=office.15)
ms:contentKeyID: 48546388
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: ad5a84dcc1765cc90fdfb08adfb6610be7057401
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/31/2018
ms.locfileid: "25879650"
---
# <a name="documentlastupdated-property-dao"></a>Document.LastUpdated Property (DAO)


**Применимо к**: Access 2013, Office 2013

Возвращает дату и время последнего изменения, внесенные в объект. Только для чтения **Variant**.

## <a name="syntax"></a>Синтаксис

*выражение* . LastUpdated

*выражение* Переменная, которая представляет собой объект- **документов** .

## <a name="remarks"></a>Замечания

**DateCreated** и **LastUpdated** возвращают дату и время создания или последнего обновления. В многопользовательской среде пользователи должны получить эти параметры непосредственно из файлового сервера, чтобы избежать несоответствия в DateCreated и параметры свойства LastUpdated.

