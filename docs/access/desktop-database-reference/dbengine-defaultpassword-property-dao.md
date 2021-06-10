---
title: Свойство DBEngine.DefaultPassword (DAO)
TOCTitle: DefaultPassword Property
ms:assetid: 189e34f3-d573-c75f-8be2-d98c50df8a52
ms:mtpsurl: https://msdn.microsoft.com/library/Ff845616(v=office.15)
ms:contentKeyID: 48543478
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 72e73d29129c749d5479e2c7b17827f13adb4847
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32294360"
---
# <a name="dbenginedefaultpassword-property-dao"></a>Свойство DBEngine.DefaultPassword (DAO)


**Область применения**: Access 2013, Office 2013

Задает пароль, используемый для создания рабочего **пространства по** умолчанию при инициализации. Для чтения и записи, **String**.

## <a name="syntax"></a>Синтаксис

*выражения* . DefaultPassword

*expression*: переменная, представляющая объект **DBEngine**.

## <a name="remarks"></a>Примечания

Параметр **DefaultPassword —** это тип данных Строки, который может иметь длину до 20 символов. Он может содержать любой символ, кроме ASCII 0.


> [!NOTE]
> Используйте надежные пароли, содержащие строчные и прописные буквы, цифры и знаки. В ненадежных паролях не используются сочетания таких элементов. Надежный пароль: Y6dh!et5. Слабый пароль: House27. Используйте надежный пароль, который можно запомнить, чтобы не пришлось его записывать.

По умолчанию свойство **DefaultUser** задает значение "admin", а **свойство DefaultPassword** — строку нулевой длины ("").

Обычно метод **CreateWorkspace** используется для создания объекта **Workspace** с заданным именем пользователя и паролем. Однако для обратной совместимости с более ранними версиями и для удобства, когда не реализована защищенная база данных, двигатель базы данных Microsoft Access автоматически создает объект **рабочей** области по умолчанию, если он еще не открыт. В этом случае значения **свойств DefaultUser** и **DefaultPassword** определяют пользователя и пароль для объекта **Рабочей области** по умолчанию.

Чтобы это свойство вступает в силу, необходимо установить его перед вызовом любых методов DAO.

