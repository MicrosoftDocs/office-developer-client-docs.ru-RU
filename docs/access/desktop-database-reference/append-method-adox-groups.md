---
title: Добавьте метод (ADOX группы)
TOCTitle: Append Method (ADOX Groups)
ms:assetid: c3245a24-55b8-3f3f-1c4a-43a119d84dc8
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249954(v=office.15)
ms:contentKeyID: 48547567
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: be31cc01122aa24eff2acb8396be2caab33c7dd4
ms.sourcegitcommit: 801b1b54786f7b0e5b0d35466e7ae8d1e840b26f
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/31/2018
ms.locfileid: "25863061"
---
# <a name="append-method-adox-groups"></a>Добавьте метод (ADOX группы)


**Применимо к**: Access 2013 | Office 2013



Добавляет новый объект [групповой](group-object-adox.md) в коллекцию [групп](groups-collection-adox.md) .

## <a name="syntax"></a>Синтаксис

*Группы*. Добавление*группы*

## <a name="parameters"></a>Параметры

  - *group*

  - Добавление объекта **группы** или имя группы для создания и добавления.

## <a name="remarks"></a>Замечания

Коллекцию **групп** [каталога](catalog-object-adox.md) предоставляет все учетные записи групп каталога. Коллекция **групп** для [пользователя](user-object-adox.md) представляет только группы, к которой принадлежит пользователь.

Если поставщик не поддерживает создание групп, произойдет ошибка.


> [!NOTE]
> Перед добавлением объекта **группы** в коллекцию **групп** объекта **пользователя** , объект **группы** с тем же [именем](name-property-adox.md) , который будет добавляться должны уже существовать в коллекцию **групп** **каталога**.


