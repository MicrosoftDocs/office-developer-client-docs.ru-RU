---
title: Свойство DBEngine.DefaultUser (DAO)
TOCTitle: DefaultUser Property
ms:assetid: 41ee0211-0794-6026-7341-3698a0b2c588
ms:mtpsurl: https://msdn.microsoft.com/library/Ff192905(v=office.15)
ms:contentKeyID: 48544464
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- dao360.chm1053071
f1_categories:
- Office.Version=v15
localization_priority: Normal
ms.openlocfilehash: c29f9663ce3591fe5b1633239e8ec0d8866ee16a
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32294350"
---
# <a name="dbenginedefaultuser-property-dao"></a>Свойство DBEngine.DefaultUser (DAO)


**Область применения**: Access 2013, Office 2013

Задает имя пользователя, используемого для создания рабочего **пространства по** умолчанию при инициализации. Для чтения и записи, **String**.

## <a name="syntax"></a>Синтаксис

*выражения* . DefaultUser

*выражение*: выражение, возвращающее объект **DBEngine**.

## <a name="remarks"></a>Примечания

Параметр **DefaultUser —** это тип данных String. Это может быть 1-20 символов в рабочей области Microsoft Access и может включать алфавитные символы, акцентные символы, цифры, пробелы и символы, за исключением: " (кавычка), / \\ (косая черта), \[ \] (назад), (скобки), : (двоеточие), | (труба), \< (меньше знака), \> (больше знака), + (плюс знак), = (знак равный), ; (semicolon), , ( запятая), ? (знак вопроса), (звездочка), ведущие пробелы и символы управления \* (ASCII 00 до ASCII 31).


> [!NOTE]
> Используйте надежные пароли, содержащие строчные и прописные буквы, цифры и знаки. В ненадежных паролях не используются сочетания таких элементов. Надежный пароль: Y6dh!et5. Слабый пароль: House27. Используйте надежный пароль, который можно запомнить, чтобы не пришлось его записывать.

По умолчанию свойство **DefaultUser** задает значение "admin", а **свойство DefaultPassword** — строку нулевой длины ("").

Имена пользователей обычно не чувствительны к делу; однако при повторном создании учетной записи пользователя, которая была удалена или создана в другой группе, имя пользователя должно быть точным совпадением исходного имени. В паролях учитывается регистр.

Обычно метод **CreateWorkspace** используется для создания объекта **Workspace** с заданным именем пользователя и паролем. Однако для обратной совместимости с более ранними версиями и для удобства, когда не реализована защищенная база данных, двигатель базы данных Microsoft Access автоматически создает объект **рабочей** области по умолчанию, если он еще не открыт. В этом случае значения **свойств DefaultUser** и **DefaultPassword** определяют пользователя и пароль для объекта **Рабочей области** по умолчанию.

Чтобы это свойство вступает в силу, необходимо установить его перед вызовом любых методов DAO.

