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
ms.openlocfilehash: b961869f3add04cf4af827f96721aad6dba611b6
ms.sourcegitcommit: 45feafb3b55de0402dddf5548c0c1c43a0eabafd
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/07/2018
ms.locfileid: "26025604"
---
# <a name="customizing-windows-registry-settings-for-the-microsoft-access-database-engine"></a><span data-ttu-id="e64a3-102">Настройка параметров реестра Windows для ядра СУБД Microsoft Access</span><span class="sxs-lookup"><span data-stu-id="e64a3-102">Customizing Windows registry settings for the Microsoft Access database engine</span></span>

<span data-ttu-id="e64a3-103">**Применимо к**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="e64a3-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="e64a3-104">Если приложение работает правильно с функциональными возможностями по умолчанию ядра базы данных Microsoft Access, может потребоваться изменить параметры в соответствии со своими потребностями реестра Microsoft Windows.</span><span class="sxs-lookup"><span data-stu-id="e64a3-104">If your application cannot work correctly with the default functionality of the Microsoft Access database engine, you may have to change the settings in the Microsoft Windows Registry to suit your needs.</span></span> <span data-ttu-id="e64a3-105">Реестра Windows можно также использовать для настройки операции устанавливаемый драйвер ISAM и ODBC.</span><span class="sxs-lookup"><span data-stu-id="e64a3-105">The Windows Registry can also be used to tune the operation of the installable ISAM and ODBC driver.</span></span>

<span data-ttu-id="e64a3-106">Можно настроить параметры реестра Windows четырьмя способами:</span><span class="sxs-lookup"><span data-stu-id="e64a3-106">You can customize the settings in the Windows Registry in four different ways:</span></span>

- [<span data-ttu-id="e64a3-107">С помощью Regedit.exe для замены параметров по умолчанию</span><span class="sxs-lookup"><span data-stu-id="e64a3-107">Using Regedit.exe to overwrite the default settings</span></span>](https://docs.microsoft.com/office/vba/access/concepts/miscellaneous/using-regedit-exe-to-overwrite-the-default-settings)
- [<span data-ttu-id="e64a3-108">Создание компонента в дереве реестра приложения для управления параметрами</span><span class="sxs-lookup"><span data-stu-id="e64a3-108">Creating a portion in your application's registry tree to manage the settings</span></span>](https://docs.microsoft.com/office/vba/access/concepts/miscellaneous/creating-a-portion-in-your-application-s-registry-tree-to-manage-the-settings)
- [<span data-ttu-id="e64a3-109">С помощью метода SetOption от DAO</span><span class="sxs-lookup"><span data-stu-id="e64a3-109">Using the SetOption method from DAO</span></span>](https://docs.microsoft.com/office/vba/access/concepts/miscellaneous/using-the-setoption-method-from-dao)
- [<span data-ttu-id="e64a3-110">С помощью свойства подключения в поставщик Microsoft OLE DB для Access</span><span class="sxs-lookup"><span data-stu-id="e64a3-110">Using the Connection properties in the Microsoft OLE DB Provider for Access</span></span>](https://docs.microsoft.com/office/vba/access/concepts/miscellaneous/using-the-connection-properties-in-the-microsoft-ole-db-provider-for-access)

