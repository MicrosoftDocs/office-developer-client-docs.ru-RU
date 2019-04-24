---
title: Свойство Document. Ластупдатед (DAO)
TOCTitle: LastUpdated Property
ms:assetid: 9307ceee-095f-0364-fd5b-905bc523b9c0
ms:mtpsurl: https://msdn.microsoft.com/library/Ff197661(v=office.15)
ms:contentKeyID: 48546388
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: abb766f7a47cbacaededf65eb2b5e9145bf88c60
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32293807"
---
# <a name="documentlastupdated-property-dao"></a>Свойство Document. Ластупдатед (DAO)


**Область применения**: Access 2013, Office 2013

Возвращает дату и время последнего изменения, внесенного в объект. Только для чтения, **Variant**.

## <a name="syntax"></a>Синтаксис

*Expression* . Ластупдатед

*Expression (выражение* ) Переменная, представляющая объект **Document** .

## <a name="remarks"></a>Замечания

**DateCreated** и **ластупдатед** возвращают дату и время создания или последнего обновления объекта. В многопользовательской среде пользователи должны получить эти параметры непосредственно с файлового сервера, чтобы избежать расхождений в параметрах свойств DateCreated и Ластупдатед.

