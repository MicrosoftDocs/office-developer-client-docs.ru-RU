---
title: Метод Append (коллекция Groups в ADOX)
TOCTitle: Append method (ADOX Groups)
ms:assetid: c3245a24-55b8-3f3f-1c4a-43a119d84dc8
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249954(v=office.15)
ms:contentKeyID: 48547567
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 9f0e7731777e3d82e3746c3886bdbddb3e43db66
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32297104"
---
# <a name="append-method-adox-groups"></a>Метод Append (коллекция Groups в ADOX)

**Область применения**: Access 2013, Office 2013

Добавляет новый [объект Group](group-object-adox.md) в коллекцию [Groups.](groups-collection-adox.md)

## <a name="syntax"></a>Синтаксис

*Группы*. Группа *приложений*

## <a name="parameters"></a>Параметры

|Параметр|Описание|
|:--------|:----------|
|*Group* |Объект **Group** для приложения или имя группы для создания и приложения.|

## <a name="remarks"></a>Примечания

Коллекция **Групп** [каталога](catalog-object-adox.md) представляет все учетные записи группы каталога. Коллекция **Groups** для [пользователя представляет](user-object-adox.md) только группу, к которой принадлежит пользователь.

Ошибка возникает, если поставщик не поддерживает создание групп.

> [!NOTE]
> Прежде чем примковать  объект **Group**  к коллекции Групп объекта Пользователя, объект **Group** с тем же именем, что и объект, который должен быть придан, уже должен существовать в коллекции **Groups** **каталога.** [](name-property-adox.md)


