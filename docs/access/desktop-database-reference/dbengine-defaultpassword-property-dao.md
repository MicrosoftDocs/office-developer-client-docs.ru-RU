---
title: DBEngine.DefaultPassword Property (DAO)
TOCTitle: DefaultPassword Property
ms:assetid: 189e34f3-d573-c75f-8be2-d98c50df8a52
ms:mtpsurl: https://msdn.microsoft.com/library/Ff845616(v=office.15)
ms:contentKeyID: 48543478
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 78610a929bd9a02c679f8e38a20f5dfcdb34ba9c
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/31/2018
ms.locfileid: "25882905"
---
# <a name="dbenginedefaultpassword-property-dao"></a>DBEngine.DefaultPassword Property (DAO)


**Применимо к**: Access 2013, Office 2013

Задает пароль, используемый для создания **рабочей области** по умолчанию при ее инициализации. Для чтения и записи, **String**.

## <a name="syntax"></a>Синтаксис

*выражение* . DefaultPassword

*выражение* Переменная, которая представляет собой объект- **DBEngine** .

## <a name="remarks"></a>Замечания

Параметр **DefaultPassword** — это тип данных String, который может иметь длину до 20 знаков. Он может содержать любой символ, за исключением ASCII 0.


> [!NOTE]
> Используйте надежные пароли, содержащие верхний и строчные буквы, числа и символы. Ненадежные пароли не смешивайте этих элементов. Надежный пароль: Y6dh! et5. Ненадежный пароль: House27. Используйте надежный пароль, который вы можете запомнить, чтобы записать его не нужно.

По умолчанию, свойство **DefaultUser** имеет значение «администратор» и **DefaultPassword** свойству в строку нулевой длины (»»).

Как правило метод **CreateWorkspace** используется для создания объекта **рабочей области** через заданное имя пользователя и пароль. Тем не менее для обеспечения обратной совместимости с предыдущими версиями и для удобства при реализации защищенной базы данных не ядро базы данных Microsoft Access автоматически создает объект **рабочей области** по умолчанию, когда требуется, если он не является open. В этом случае значения свойств **DefaultUser** и **DefaultPassword** определить имя пользователя и пароль для объекта **рабочей области** по умолчанию.

Для этого свойства вступили в силу следует устанавливать до вызова метода любые методы DAO.

