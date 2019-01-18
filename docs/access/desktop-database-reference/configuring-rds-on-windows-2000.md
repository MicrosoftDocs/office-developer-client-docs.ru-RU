---
title: Настройка RDS в Windows 2000
TOCTitle: Configuring RDS on Windows 2000
ms:assetid: eb2d4c1d-8b3b-07ac-258f-edb0b1a3daba
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250193(v=office.15)
ms:contentKeyID: 48548482
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 8482df5ca2fab110e5b1a77fe227c5f0c583d893
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/17/2019
ms.locfileid: "28720956"
---
# <a name="configuring-rds-on-windows-2000"></a><span data-ttu-id="4280a-102">Настройка RDS в Windows 2000</span><span class="sxs-lookup"><span data-stu-id="4280a-102">Configuring RDS on Windows 2000</span></span>


<span data-ttu-id="4280a-103">**Применимо к**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="4280a-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="4280a-104">При возникновении затруднений при получении служб удаленных рабочих СТОЛОВ для правильной работы после обновления до Windows 2000, выполните следующие шаги для устранения неполадок.</span><span class="sxs-lookup"><span data-stu-id="4280a-104">If you experience difficulties getting RDS to function properly after upgrading to Windows 2000, follow the steps below to troubleshoot the issue.</span></span>

1.  <span data-ttu-id="4280a-105">Убедитесь в том, что служба IIS запущен первый перейдя к https://*сервера* с помощью Internet Explorer.</span><span class="sxs-lookup"><span data-stu-id="4280a-105">Make sure that the World Wide Web Publishing Service is running first by navigating to https://*server* using Internet Explorer.</span></span> <span data-ttu-id="4280a-106">Если не удается получить доступ к веб-сервера таким образом, запустите из командной строки и введите следующую команду «NET НАЧАТЬ W3SVC».</span><span class="sxs-lookup"><span data-stu-id="4280a-106">If you are unable to access the web server this way, go to a command prompt and enter the following command, "NET START W3SVC".</span></span>

2.  <span data-ttu-id="4280a-107">В меню Пуск выберите команду выполнить.</span><span class="sxs-lookup"><span data-stu-id="4280a-107">From the Start menu, select Run.</span></span> <span data-ttu-id="4280a-108">Введите msdfmap.ini и нажмите кнопку ОК, чтобы открыть файл msdfmap.ini в "Блокнот".</span><span class="sxs-lookup"><span data-stu-id="4280a-108">Type msdfmap.ini and click OK to open the msdfmap.ini file in Notepad.</span></span> <span data-ttu-id="4280a-109">Проверка \[ПОДКЛЮЧЕНИЕ по умолчанию\] и если параметр доступа — это значение NOACCESS, измените его только для чтения.</span><span class="sxs-lookup"><span data-stu-id="4280a-109">Check the \[CONNECT DEFAULT\] section, and if the ACCESS parameter is set to NOACCESS, change it to READONLY.</span></span>

3.  <span data-ttu-id="4280a-110">С помощью служебной программы RegEdit, перейдите к «HKEY\_ЛОКАЛЬНОГО\_МАШИНЫ\\программного обеспечения\\Microsoft\\DataFactory\\HandlerInfo» и убедитесь, что **HandlerRequired** имеет значение 0 и **DefaultHandler** — это «» (значение Null Строковое значение).</span><span class="sxs-lookup"><span data-stu-id="4280a-110">Using the RegEdit utility, navigate to "HKEY\_LOCAL\_MACHINE\\SOFTWARE\\Microsoft\\DataFactory\\HandlerInfo" and make sure **HandlerRequired** is set to 0 and **DefaultHandler** is "" (Null string).</span></span>
    
    > [!NOTE]
    > <span data-ttu-id="4280a-111">При внесении изменений в этот раздел реестра, необходимо остановить и перезапустить службу веб-публикации, введя следующие команды в командной строке: «NET STOP W3SVC» и «W3SVC ЗАПУСТИТЕ NET».</span><span class="sxs-lookup"><span data-stu-id="4280a-111">If you make any changes to this section of the registry, you must stop and restart the World Wide Web Publishing Service by entering the following commands at a command prompt: "NET STOP W3SVC" and "NET START W3SVC".</span></span>

4.  <span data-ttu-id="4280a-112">С помощью служебной программы RegEdit, перейдите в реестр, чтобы «HKEY\_ЛОКАЛЬНОГО\_МАШИНЫ\\системы\\CurrentControlSet\\служб\\W3SVC\\параметры\\ADCLaunch» и убедитесь, что основные называемое \*\* RDSServer.Datafactory\*\*.</span><span class="sxs-lookup"><span data-stu-id="4280a-112">Using the RegEdit utility, navigate in the registry to "HKEY\_LOCAL\_MACHINE\\SYSTEM\\CurrentControlSet\\Services\\W3SVC\\Parameters\\ADCLaunch" and verify that there is a key called **RDSServer.Datafactory**.</span></span> <span data-ttu-id="4280a-113">Если нет, создайте его.</span><span class="sxs-lookup"><span data-stu-id="4280a-113">If not, create it.</span></span>

5.  <span data-ttu-id="4280a-114">С помощью диспетчера служб Интернета, перейдите на веб-сайт по умолчанию и просмотра свойств виртуального корня службу.</span><span class="sxs-lookup"><span data-stu-id="4280a-114">Using Internet Services Manager, go to the default website and view the properties of the MSADC virtual root.</span></span> <span data-ttu-id="4280a-115">Проверьте каталог безопасности и IP-адреса и ограничения именования домена.</span><span class="sxs-lookup"><span data-stu-id="4280a-115">Inspect the Directory Security/IP Address and Domain Name Restrictions.</span></span> <span data-ttu-id="4280a-116">Если установлен флажок «доступ запрещен» выберите пункт «Разрешен».</span><span class="sxs-lookup"><span data-stu-id="4280a-116">If the "Access is Denied" is checked then select "Granted".</span></span>

<span data-ttu-id="4280a-117">Убедитесь, что для пробного перезагрузка сервера, если изменения не будут отображаться для решения проблемы в первую очередь.</span><span class="sxs-lookup"><span data-stu-id="4280a-117">Be sure to try rebooting the server if the changes to do not appear to solve the problem at first.</span></span>

