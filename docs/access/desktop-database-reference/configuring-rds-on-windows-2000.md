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
# <a name="configuring-rds-on-windows-2000"></a><span data-ttu-id="87102-102">Настройка RDS в Windows 2000</span><span class="sxs-lookup"><span data-stu-id="87102-102">Configuring RDS on Windows 2000</span></span>


<span data-ttu-id="87102-103">**Область применения**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="87102-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="87102-104">Если после обновления до 2000 года Windows RDS, выполните следующие действия, чтобы устранить проблему.</span><span class="sxs-lookup"><span data-stu-id="87102-104">If you experience difficulties getting RDS to function properly after upgrading to Windows 2000, follow the steps below to troubleshoot the issue.</span></span>

1.  <span data-ttu-id="87102-105">Убедитесь, что служба публикации world Wide Web запущена сначала, перенавигавшись на https://*с* помощью Internet Explorer.</span><span class="sxs-lookup"><span data-stu-id="87102-105">Make sure that the World Wide Web Publishing Service is running first by navigating to https://*server* using Internet Explorer.</span></span> <span data-ttu-id="87102-106">Если таким образом вы не можете получить доступ к веб-серверу, перейдите к командной подсказке и введите следующую команду: "NET START W3SVC".</span><span class="sxs-lookup"><span data-stu-id="87102-106">If you are unable to access the web server this way, go to a command prompt and enter the following command, "NET START W3SVC".</span></span>

2.  <span data-ttu-id="87102-107">Из меню "Пуск" выберите Выполнить.</span><span class="sxs-lookup"><span data-stu-id="87102-107">From the Start menu, select Run.</span></span> <span data-ttu-id="87102-108">Введите msdfmap.ini и нажмите кнопку ОК, чтобы открыть msdfmap.ini в Блокнот.</span><span class="sxs-lookup"><span data-stu-id="87102-108">Type msdfmap.ini and click OK to open the msdfmap.ini file in Notepad.</span></span> <span data-ttu-id="87102-109">Проверьте раздел CONNECT DEFAULT, и если параметр ACCESS задан \[ \] в NOACCESS, измените его на READONLY.</span><span class="sxs-lookup"><span data-stu-id="87102-109">Check the \[CONNECT DEFAULT\] section, and if the ACCESS parameter is set to NOACCESS, change it to READONLY.</span></span>

3.  <span data-ttu-id="87102-110">С помощью утилиты RegEdit перейдите в "HKEY \_ LOCAL MACHINE SOFTWARE Microsoft DataFactory HandlerInfo" и убедитесь, что значение \_ \\ \\ \\ \\ **HandlerRequired** равно 0, а **DefaultHandler** — "" (строка Null).</span><span class="sxs-lookup"><span data-stu-id="87102-110">Using the RegEdit utility, navigate to "HKEY\_LOCAL\_MACHINE\\SOFTWARE\\Microsoft\\DataFactory\\HandlerInfo" and make sure **HandlerRequired** is set to 0 and **DefaultHandler** is "" (Null string).</span></span>
    
    > [!NOTE]
    > <span data-ttu-id="87102-111">При внесении изменений в этот раздел реестра необходимо остановить и перезапустить службу публикации World Wide Web Publishing Service, введите следующие команды по командной подсказке: "NET STOP W3SVC" и "NET START W3SVC".</span><span class="sxs-lookup"><span data-stu-id="87102-111">If you make any changes to this section of the registry, you must stop and restart the World Wide Web Publishing Service by entering the following commands at a command prompt: "NET STOP W3SVC" and "NET START W3SVC".</span></span>

4.  <span data-ttu-id="87102-112">Используя утилиту RegEdit, перейдите в реестр по ссылке "HKEY \_ LOCAL \_ MACHINE SYSTEM \\ \\ CurrentControlSet Services W3SVC Parameters ADCLaunch" и убедитесь, что есть ключ под названием \\ \\ \\ \\ **RDSServer.Datafactory**.</span><span class="sxs-lookup"><span data-stu-id="87102-112">Using the RegEdit utility, navigate in the registry to "HKEY\_LOCAL\_MACHINE\\SYSTEM\\CurrentControlSet\\Services\\W3SVC\\Parameters\\ADCLaunch" and verify that there is a key called **RDSServer.Datafactory**.</span></span> <span data-ttu-id="87102-113">Если нет, создайте его.</span><span class="sxs-lookup"><span data-stu-id="87102-113">If not, create it.</span></span>

5.  <span data-ttu-id="87102-114">С помощью диспетчера интернет-служб перейдите на веб-сайт по умолчанию и просмотреть свойства виртуального корневого корня MSADC.</span><span class="sxs-lookup"><span data-stu-id="87102-114">Using Internet Services Manager, go to the default website and view the properties of the MSADC virtual root.</span></span> <span data-ttu-id="87102-115">Проверьте ограничения безопасности каталога и IP-адресов и доменных имен.</span><span class="sxs-lookup"><span data-stu-id="87102-115">Inspect the Directory Security/IP Address and Domain Name Restrictions.</span></span> <span data-ttu-id="87102-116">Если "Доступ отказано" проверяется, выберите "Предоставлено".</span><span class="sxs-lookup"><span data-stu-id="87102-116">If the "Access is Denied" is checked then select "Granted".</span></span>

<span data-ttu-id="87102-117">Попробуйте перезагрузать сервер, если изменения сначала не решат проблему.</span><span class="sxs-lookup"><span data-stu-id="87102-117">Be sure to try rebooting the server if the changes to do not appear to solve the problem at first.</span></span>

