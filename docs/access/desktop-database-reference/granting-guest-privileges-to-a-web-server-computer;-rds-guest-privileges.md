---
title: Предоставление гостевых привилегий компьютеру веб-сервера; Гостевых привилегий RDS
TOCTitle: Granting guest privileges to a web server computer; RDS guest privileges
ms:assetid: 4ec9c05b-36f6-de22-b848-0cb8573f9dd1
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249254(v=office.15)
ms:contentKeyID: 48544766
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 8c0ee29125bf06ef51d1ac511838bdd09231e1a6
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32292127"
---
# <a name="granting-guest-privileges-to-a-web-server-computer-rds-guest-privileges"></a>Предоставление гостевых привилегий компьютеру с веб-сервером; Гостевых привилегий RDS

**Область применения**: Access 2013, Office 2013

Учетная запись анонимного веб-сервера (IUSR ComputerName) должна быть добавлена в локализованную группу "Гости" на компьютере веб-сервера для \_ использования RDS.

**Предоставление гостевых привилегий компьютеру веб-сервера**

1.  На компьютере с Microsoft Windows 2000 Server нажмите кнопку **"Начните"** и выберите пункты "Программы", "Администрирование" и "Управление   **компьютером".**

2.  В дереве консоли в области **"Локальные пользователи и группы"** щелкните **"Группы".**

3.  Выберите **локализованную группу "Гости".** В меню **"Действие"** выберите **"Свойства".**

4.  В **диалоговом окне "Свойства** гостей" нажмите кнопку **"Добавить".**

5.  Если учетная запись анонимного веб-сервера  не появляется в списке в диалоговом окне "Выбор пользователей или групп", введите ее имя (IUSR \_ *ComputerName)* в нижнее пустое поле и нажмите кнопку **"Добавить".**

6.  Нажмите кнопку **ОК**.

