---
title: Append Method (ADOX Views)
TOCTitle: Append Method (ADOX Views)
ms:assetid: 202f1d0a-dc5d-84e5-daf3-3212e5bc6088
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248985(v=office.15)
ms:contentKeyID: 48543655
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 106dd9d72cb350422f00da05859bc096cb2b52e9
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/09/2018
ms.locfileid: "25481505"
---
# <a name="append-method-adox-views"></a>Append Method (ADOX Views)


**Применимо к**: Access 2013 | Office 2013


Создает новый объект [представления](view-object-adox.md) и добавляет его в коллекцию [представлений](views-collection-adox.md) .

## <a name="syntax"></a>Синтаксис

*Представления*. Добавьте*имя*, *команда*

## <a name="parameters"></a>Параметры

  - *Имя*

  - **Строковое** значение, задающее имя представления для создания.

  - *Команда*

  - Объект ADO [команды](command-object-ado.md) , представляющий представление для создания.

## <a name="remarks"></a>Замечания

Создает новое представление источника данных с именем и атрибуты, указанные в объекте **команды** .

Если текст команды, который пользователь вводит представляет процедуры, а не как представление, поведение зависит от поставщика. **Добавление** завершится ошибкой, если поставщик не поддерживает сохранение команды.


> [!NOTE]
> <P>При использовании поставщика OLE DB для Microsoft Jet, коллекции <STRONG>представлений</STRONG> метод <STRONG>Append</STRONG> позволит можно использовать для определения <STRONG>процедуры</STRONG> , а не в <STRONG>представлении</STRONG> с помощью параметра <EM>командной</EM> . <STRONG>Процедуры</STRONG> добавляются к источнику данных и добавляются в коллекцию <STRONG>представлений</STRONG> . После <STRONG>добавления</STRONG>при обновлении семейств сайтов <STRONG>процедуры</STRONG> и <STRONG>представления</STRONG> <STRONG>процедуры</STRONG> больше не будет находиться в коллекции <STRONG>представлений</STRONG> и будет отображаться в коллекции <STRONG>процедур</STRONG> .</P>


