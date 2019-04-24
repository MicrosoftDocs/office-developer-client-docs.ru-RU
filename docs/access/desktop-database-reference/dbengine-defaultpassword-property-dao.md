---
title: Свойство DBEngine. DefaultPassword (DAO)
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
# <a name="dbenginedefaultpassword-property-dao"></a>Свойство DBEngine. DefaultPassword (DAO)


**Область применения**: Access 2013, Office 2013

Задает пароль, используемый для создания **рабочей области** по умолчанию при ее инициализации. Для чтения и записи, **String**.

## <a name="syntax"></a>Синтаксис

*Expression* . DefaultPassword

*Expression (выражение* ) Переменная, представляющая объект **DBEngine** .

## <a name="remarks"></a>Замечания

Параметр **DefaultPassword** имеет тип данных String, длина которого не может превышать 20 символов. Он может содержать любой символ, кроме ASCII 0.


> [!NOTE]
> Используйте надежные пароли, объединяющие прописные и строчные буквы, цифры и символы. В слабых паролях эти элементы не комбинируются. Надежный пароль: Y6dh!et5. Слабый пароль: House27. Используйте надежный пароль, который можно запомнить, чтобы не записывать его.

По умолчанию для свойства **DefaultUser** задано значение "admin", а для свойства **DefaultPassword** задана строка нулевой длины ("").

Как правило, метод **CreateWorkspace** используется для создания объекта **Workspace** с заданными именем пользователя и паролем. Однако для обеспечения обратной совместимости с более ранними версиями и удобства при отсутствии защищенной базы данных ядро СУБД Microsoft Access автоматически создает объект **рабочей области** по умолчанию, если он еще не открыт. В этом случае значения свойств **DefaultUser** и **DefaultPassword** определяют пользователя и пароль для объекта **рабочей области** по умолчанию.

Чтобы это свойство вступило в силу, необходимо задать его перед вызовом методов DAO.

