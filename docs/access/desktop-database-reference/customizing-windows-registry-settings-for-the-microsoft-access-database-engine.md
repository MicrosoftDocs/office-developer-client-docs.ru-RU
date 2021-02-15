---
title: Настройка параметров реестра Windows для ядра СУБД Microsoft Access
TOCTitle: Customizing Windows registry settings for the Microsoft Access database engine
ms:assetid: ca7e958a-ea26-d67d-45b9-10aeb1eac96b
ms:mtpsurl: https://msdn.microsoft.com/library/Ff834346(v=office.15)
ms:contentKeyID: 48547690
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- acmain11.chm1032168
f1_categories:
- Office.Version=v15
localization_priority: Normal
ms.openlocfilehash: 7cbe8ad56e01249563f7b06c9018d923a96246e9
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32295123"
---
# <a name="customizing-windows-registry-settings-for-the-microsoft-access-database-engine"></a><span data-ttu-id="34e47-102">Настройка параметров реестра Windows для ядра СУБД Microsoft Access</span><span class="sxs-lookup"><span data-stu-id="34e47-102">Customizing Windows registry settings for the Microsoft Access database engine</span></span>

<span data-ttu-id="34e47-103">**Область применения**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="34e47-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="34e47-104">Если приложение не может правильно работать с функциями якоря базы данных Microsoft Access по умолчанию, может потребоваться изменить параметры реестра Microsoft Windows в соответствии со своими потребностями.</span><span class="sxs-lookup"><span data-stu-id="34e47-104">If your application cannot work correctly with the default functionality of the Microsoft Access database engine, you may have to change the settings in the Microsoft Windows Registry to suit your needs.</span></span> <span data-ttu-id="34e47-105">Реестр Windows также можно использовать для настройки работы устанавливаемого драйвера ISAM и ODBC.</span><span class="sxs-lookup"><span data-stu-id="34e47-105">The Windows Registry can also be used to tune the operation of the installable ISAM and ODBC driver.</span></span>

<span data-ttu-id="34e47-106">Параметры в реестре Windows можно настроить четырьмя способами:</span><span class="sxs-lookup"><span data-stu-id="34e47-106">You can customize the settings in the Windows Registry in four different ways:</span></span>

- [<span data-ttu-id="34e47-107">Использование Regedit.exe для переоценки параметров по умолчанию</span><span class="sxs-lookup"><span data-stu-id="34e47-107">Using Regedit.exe to overwrite the default settings</span></span>](https://docs.microsoft.com/office/vba/access/concepts/miscellaneous/using-regedit-exe-to-overwrite-the-default-settings)
- [<span data-ttu-id="34e47-108">Создание части в дереве реестра приложения для управления настройками</span><span class="sxs-lookup"><span data-stu-id="34e47-108">Creating a portion in your application's registry tree to manage the settings</span></span>](https://docs.microsoft.com/office/vba/access/concepts/miscellaneous/creating-a-portion-in-your-application-s-registry-tree-to-manage-the-settings)
- [<span data-ttu-id="34e47-109">Использование метода SetOption из DAO</span><span class="sxs-lookup"><span data-stu-id="34e47-109">Using the SetOption method from DAO</span></span>](https://docs.microsoft.com/office/vba/access/concepts/miscellaneous/using-the-setoption-method-from-dao)
- [<span data-ttu-id="34e47-110">Использование свойств подключения в поставщике Microsoft OLE DB для Access</span><span class="sxs-lookup"><span data-stu-id="34e47-110">Using the Connection properties in the Microsoft OLE DB Provider for Access</span></span>](https://docs.microsoft.com/office/vba/access/concepts/miscellaneous/using-the-connection-properties-in-the-microsoft-ole-db-provider-for-access)

