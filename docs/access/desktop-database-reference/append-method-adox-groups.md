---
title: Метод Append (коллекция Groups в ADOX)
TOCTitle: Append method (ADOX Groups)
ms:assetid: c3245a24-55b8-3f3f-1c4a-43a119d84dc8
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249954(v=office.15)
ms:contentKeyID: 48547567
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: d552539b84972b4a20fe0bff39b6c8570719bcf7
ms.sourcegitcommit: 980a96cf444882d3d34cecb5faac8f8a7b7c4b57
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/03/2018
ms.locfileid: "25950162"
---
# <a name="append-method-adox-groups"></a>Метод Append (коллекция Groups в ADOX)

**Применимо к**: Access 2013, Office 2013

Добавляет новый объект [групповой](group-object-adox.md) в коллекцию [групп](groups-collection-adox.md) .

## <a name="syntax"></a>Синтаксис

*Группы*. Добавление*группы*

## <a name="parameters"></a>Параметры

|Параметр|Описание|
|:--------|:----------|
|*Group* |Добавление объекта **группы** или имя группы для создания и добавления.|

## <a name="remarks"></a>Примечания

Коллекцию **групп** [каталога](catalog-object-adox.md) предоставляет все учетные записи групп каталога. Коллекция **групп** для [пользователя](user-object-adox.md) представляет только группы, к которой принадлежит пользователь.

Если поставщик не поддерживает создание групп, произойдет ошибка.

> [!NOTE]
> Перед добавлением объекта **группы** в коллекцию **групп** объекта **пользователя** , объект **группы** с тем же [именем](name-property-adox.md) , который будет добавляться должны уже существовать в коллекцию **групп** **каталога**.


