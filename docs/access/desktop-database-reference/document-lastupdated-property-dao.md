---
title: Свойство Document.LastUpdated (DAO)
TOCTitle: LastUpdated Property
ms:assetid: 9307ceee-095f-0364-fd5b-905bc523b9c0
ms:mtpsurl: https://msdn.microsoft.com/library/Ff197661(v=office.15)
ms:contentKeyID: 48546388
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 57fb558330c602206831c1c72f09a13094eba799
ms.sourcegitcommit: d7248f803002b31cf7fc561b03530199a9b0a8fd
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/02/2018
ms.locfileid: "25927314"
---
# <a name="documentlastupdated-property-dao"></a>Свойство Document.LastUpdated (DAO)


**Применимо к**: Access 2013, Office 2013

Возвращает дату и время последнего изменения, внесенные в объект. Только для чтения **Variant**.

## <a name="syntax"></a>Синтаксис

*выражение* . LastUpdated

*выражение* Переменная, которая представляет собой объект- **документов** .

## <a name="remarks"></a>Примечания

**DateCreated** и **LastUpdated** возвращают дату и время создания или последнего обновления. В многопользовательской среде пользователи должны получить эти параметры непосредственно из файлового сервера, чтобы избежать несоответствия в DateCreated и параметры свойства LastUpdated.

