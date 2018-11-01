---
title: Настройка параметров реестра Windows для ядро СУБД Microsoft Access
TOCTitle: Customizing Windows Registry Settings for the Microsoft Access Database Engine
ms:assetid: ca7e958a-ea26-d67d-45b9-10aeb1eac96b
ms:mtpsurl: https://msdn.microsoft.com/library/Ff834346(v=office.15)
ms:contentKeyID: 48547690
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- acmain11.chm1032168
f1_categories:
- Office.Version=v15
ms.openlocfilehash: a44226e8ea90a8be96de35cdc923349eded17cb4
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/31/2018
ms.locfileid: "25887000"
---
# <a name="customizing-windows-registry-settings-for-the-microsoft-access-database-engine"></a><span data-ttu-id="9bb04-102">Настройка параметров реестра Windows для ядро базы данных Microsoft Access</span><span class="sxs-lookup"><span data-stu-id="9bb04-102">Customizing Windows Registry Settings for the Microsoft Access Database Engine</span></span>


<span data-ttu-id="9bb04-103">**Применимо к**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="9bb04-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="9bb04-104">Если приложение работает правильно с функциональными возможностями по умолчанию ядра базы данных Microsoft Access, может потребоваться изменить параметры реестра Microsoft® Windows® в соответствии со своими потребностями.</span><span class="sxs-lookup"><span data-stu-id="9bb04-104">If your application cannot work correctly with the default functionality of the Microsoft Access database engine, you may have to change the settings in the Microsoft® Windows® Registry to suit your needs.</span></span> <span data-ttu-id="9bb04-105">Реестра Windows можно также использовать для настройки операции устанавливаемый драйвер ISAM и ODBC.</span><span class="sxs-lookup"><span data-stu-id="9bb04-105">The Windows Registry can also be used to tune the operation of the installable ISAM and ODBC driver.</span></span>

<span data-ttu-id="9bb04-106">Можно настроить параметры реестра Windows четырьмя способами:</span><span class="sxs-lookup"><span data-stu-id="9bb04-106">You can customize the settings in the Windows Registry in four different ways:</span></span>

<span data-ttu-id="9bb04-107">[С помощью Regedit.exe для замены параметров по умолчанию](https://msdn.microsoft.com/library/ff193205\(v=office.15\))</span><span class="sxs-lookup"><span data-stu-id="9bb04-107">[Using Regedit.exe to Overwrite the Default Settings](https://msdn.microsoft.com/library/ff193205\(v=office.15\))</span></span>

<span data-ttu-id="9bb04-108">[Создание компонента в дереве реестра приложения для управления параметрами](https://msdn.microsoft.com/library/ff836342\(v=office.15\))</span><span class="sxs-lookup"><span data-stu-id="9bb04-108">[Creating a Portion in Your Application's Registry Tree to Manage the Settings](https://msdn.microsoft.com/library/ff836342\(v=office.15\))</span></span>

<span data-ttu-id="9bb04-109">[С помощью метода SetOption от DAO](https://msdn.microsoft.com/library/ff194471\(v=office.15\))</span><span class="sxs-lookup"><span data-stu-id="9bb04-109">[Using the SetOption Method from DAO](https://msdn.microsoft.com/library/ff194471\(v=office.15\))</span></span>

<span data-ttu-id="9bb04-110">[С помощью свойства подключения в поставщик Microsoft OLE DB для Access](https://msdn.microsoft.com/library/ff196356\(v=office.15\))</span><span class="sxs-lookup"><span data-stu-id="9bb04-110">[Using the Connection Properties in the Microsoft OLE DB Provider for Access](https://msdn.microsoft.com/library/ff196356\(v=office.15\))</span></span>

