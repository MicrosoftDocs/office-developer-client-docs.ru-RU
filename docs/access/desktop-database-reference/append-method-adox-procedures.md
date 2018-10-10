---
title: Append Method (ADOX Procedures)
TOCTitle: Append Method (ADOX Procedures)
ms:assetid: a93b31bb-e41a-5152-abe7-dd7c2b2fcd0a
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249783(v=office.15)
ms:contentKeyID: 48546919
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 5c1afc7aeea90fc152df7d8f7b1601bf3753b3a3
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/09/2018
ms.locfileid: "25480124"
---
# <a name="append-method-adox-procedures"></a>Append Method (ADOX Procedures)


**Применимо к**: Access 2013 | Office 2013


Добавляет новый объект [процедуры](procedure-object-adox.md) в коллекцию [процедур](procedures-collection-adox.md) .

## <a name="syntax"></a>Синтаксис

*Процедуры*. Добавьте*имя*, *команда*

## <a name="parameters"></a>Параметры

  - *Имя*

  - **Строковое** значение, задающее имя процедуры для создания и добавления.

  - *Команда*

  - Объект ADO [команды](command-object-ado.md) , который представляет процедуры для создания и добавления.

## <a name="remarks"></a>Замечания

Создает новую процедуру в источник данных с именем и атрибуты, указанные в объекте **команды** .

Если текст команды, который пользователь вводит представляет представления, а не процедуры, поведение зависит от используемого поставщика. **Добавление** завершится ошибкой, если поставщик не поддерживает сохранение команды.


> [!NOTE]
> <P>При использовании поставщика OLE DB для Microsoft Jet, позволит метод <STRONG>Append</STRONG> коллекции <STRONG>процедуры</STRONG> можно использовать для определения <STRONG>представления</STRONG> , а не на <STRONG>процедуру</STRONG> с помощью параметра <EM>командной</EM> . <STRONG>Представление</STRONG> будет добавлен к источнику данных и добавляются в коллекцию <STRONG>процедур</STRONG> . После <STRONG>добавления</STRONG>при обновлении семейств сайтов <STRONG>процедуры</STRONG> и <STRONG>представления</STRONG> , <STRONG>представление</STRONG> больше не будет находиться в коллекции <STRONG>процедуры</STRONG> и будет отображаться в коллекции <STRONG>представлений</STRONG> .</P>


