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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32296019"
---
# <a name="configuring-rds-on-windows-2000"></a><span data-ttu-id="e01d2-102">Настройка RDS в Windows 2000</span><span class="sxs-lookup"><span data-stu-id="e01d2-102">Configuring RDS on Windows 2000</span></span>


<span data-ttu-id="e01d2-103">**Область применения**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="e01d2-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="e01d2-104">Если у вас возникают проблемы при попытке правильной работы RDS после обновления до Windows 2000, выполните указанные ниже действия, чтобы устранить эту проблему.</span><span class="sxs-lookup"><span data-stu-id="e01d2-104">If you experience difficulties getting RDS to function properly after upgrading to Windows 2000, follow the steps below to troubleshoot the issue.</span></span>

1.  <span data-ttu-id="e01d2-105">Убедитесь, что служба веб-публикации запущена первым путем перехода на*сервер* HTTPS://с помощью Internet Explorer.</span><span class="sxs-lookup"><span data-stu-id="e01d2-105">Make sure that the World Wide Web Publishing Service is running first by navigating to https://*server* using Internet Explorer.</span></span> <span data-ttu-id="e01d2-106">Если вы не можете получить доступ к веб-серверу таким образом, перейдите в окно командной строки и введите следующую команду: "NET START W3SVC".</span><span class="sxs-lookup"><span data-stu-id="e01d2-106">If you are unable to access the web server this way, go to a command prompt and enter the following command, "NET START W3SVC".</span></span>

2.  <span data-ttu-id="e01d2-107">В меню Пуск выберите команду выполнить.</span><span class="sxs-lookup"><span data-stu-id="e01d2-107">From the Start menu, select Run.</span></span> <span data-ttu-id="e01d2-108">Введите мсдфмап. ini и нажмите кнопку ОК, чтобы открыть файл мсдфмап. ini в блокноте.</span><span class="sxs-lookup"><span data-stu-id="e01d2-108">Type msdfmap.ini and click OK to open the msdfmap.ini file in Notepad.</span></span> <span data-ttu-id="e01d2-109">Установите флажок \[подключиться к\] разделу по умолчанию, а если параметру Access присвоено значение "недоступно", измените его на ReadOnly.</span><span class="sxs-lookup"><span data-stu-id="e01d2-109">Check the \[CONNECT DEFAULT\] section, and if the ACCESS parameter is set to NOACCESS, change it to READONLY.</span></span>

3.  <span data-ttu-id="e01d2-110">С помощью программы regedit перейдите к разделу\_"\_программное\\обеспечение\\локального компьютера\\(\\Microsoft Хандлеринфо, Microsoft. **хандлеррекуиред** ") и убедитесь, что для задано значение 0, а **дефаулсандлер** — "" (нулевая строка).</span><span class="sxs-lookup"><span data-stu-id="e01d2-110">Using the RegEdit utility, navigate to "HKEY\_LOCAL\_MACHINE\\SOFTWARE\\Microsoft\\DataFactory\\HandlerInfo" and make sure **HandlerRequired** is set to 0 and **DefaultHandler** is "" (Null string).</span></span>
    
    > [!NOTE]
    > <span data-ttu-id="e01d2-111">Если вы вносите изменения в этот раздел реестра, необходимо остановить и перезапустить службу публикации в Интернете, введя следующие команды в командной строки: "NET STOP W3SVC" и "NET START W3SVC".</span><span class="sxs-lookup"><span data-stu-id="e01d2-111">If you make any changes to this section of the registry, you must stop and restart the World Wide Web Publishing Service by entering the following commands at a command prompt: "NET STOP W3SVC" and "NET START W3SVC".</span></span>

4.  <span data-ttu-id="e01d2-112">С помощью программы Regedit переместитесь в реестре "CurrentControlSet\_Local\_Machine\\System\\Services\\\\Services\\\\адклаунч" и убедитесь, что существует ключ с именем **рдссервер.. факт**.</span><span class="sxs-lookup"><span data-stu-id="e01d2-112">Using the RegEdit utility, navigate in the registry to "HKEY\_LOCAL\_MACHINE\\SYSTEM\\CurrentControlSet\\Services\\W3SVC\\Parameters\\ADCLaunch" and verify that there is a key called **RDSServer.Datafactory**.</span></span> <span data-ttu-id="e01d2-113">Если это не так, создайте его.</span><span class="sxs-lookup"><span data-stu-id="e01d2-113">If not, create it.</span></span>

5.  <span data-ttu-id="e01d2-114">С помощью диспетчера служб Интернета перейдите на веб-сайт по умолчанию и просмотрите свойства виртуального корневого каталога MSADC.</span><span class="sxs-lookup"><span data-stu-id="e01d2-114">Using Internet Services Manager, go to the default website and view the properties of the MSADC virtual root.</span></span> <span data-ttu-id="e01d2-115">Проверьте ограничения на безопасность/IP-адрес и доменное имя каталога.</span><span class="sxs-lookup"><span data-stu-id="e01d2-115">Inspect the Directory Security/IP Address and Domain Name Restrictions.</span></span> <span data-ttu-id="e01d2-116">Если флажок "отказано в доступе" установлен, выберите пункт "предоставлено".</span><span class="sxs-lookup"><span data-stu-id="e01d2-116">If the "Access is Denied" is checked then select "Granted".</span></span>

<span data-ttu-id="e01d2-117">Не забудьте попробовать перегрузить сервер, если изменения, которые не будут отображаться, не помогли в начале проблемы.</span><span class="sxs-lookup"><span data-stu-id="e01d2-117">Be sure to try rebooting the server if the changes to do not appear to solve the problem at first.</span></span>

