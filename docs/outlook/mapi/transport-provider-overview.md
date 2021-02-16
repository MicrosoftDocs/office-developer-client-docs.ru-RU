---
title: Обзор поставщика транспорта
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: a51547e6-8f0e-45f4-a341-3cfa735112c2
description: 'Дата последнего изменения: 23 июля 2011 г.'
ms.openlocfilehash: 53bdba624ba759debba25bae78fb45b0f9d5247e
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33433159"
---
# <a name="transport-provider-overview"></a><span data-ttu-id="c98d1-103">Обзор поставщика транспорта</span><span class="sxs-lookup"><span data-stu-id="c98d1-103">Transport Provider Overview</span></span>

  
  
<span data-ttu-id="c98d1-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="c98d1-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="c98d1-105">Поставщик транспорта — это библиотека динамической связи (DLL), которая выступает в качестве посредника между подсистемой MAPI и одной или более систем обмена сообщениями.</span><span class="sxs-lookup"><span data-stu-id="c98d1-105">A transport provider is a dynamic-link library (DLL) which acts as an intermediary between the MAPI subsystem and one or more underlying messaging systems.</span></span> <span data-ttu-id="c98d1-106">Система обмена сообщениями — это определенный механизм, с помощью которого отправляются и получаются сообщения.</span><span class="sxs-lookup"><span data-stu-id="c98d1-106">A messaging system is some specific mechanism by which messages are sent and received.</span></span> <span data-ttu-id="c98d1-107">Вот несколько примеров систем обмена сообщениями:</span><span class="sxs-lookup"><span data-stu-id="c98d1-107">Some examples of messaging systems are:</span></span>
  
- <span data-ttu-id="c98d1-108">Общая файловая система сети, в которую поставщик транспорта записывает сообщения напрямую.</span><span class="sxs-lookup"><span data-stu-id="c98d1-108">A shared network file system that the transport provider writes messages to directly.</span></span>
    
- <span data-ttu-id="c98d1-109">Сетевой интерфейс TCP/IP, который поставщик транспорта использует для подключения к серверу обмена сообщениями.</span><span class="sxs-lookup"><span data-stu-id="c98d1-109">A TCP/IP network interface that the transport provider uses to connect to a messaging server.</span></span>
    
- <span data-ttu-id="c98d1-110">Веб-служба, к которую подключаются пользователи.</span><span class="sxs-lookup"><span data-stu-id="c98d1-110">An online service that users connect to.</span></span>
    
- <span data-ttu-id="c98d1-111">Система обмена сообщениями на основе хост-приложений или системы автоматизации Office.</span><span class="sxs-lookup"><span data-stu-id="c98d1-111">A host-based messaging or office automation system.</span></span>
    
- <span data-ttu-id="c98d1-112">Набор удаленных вызовов процедур на сервер обмена сообщениями.</span><span class="sxs-lookup"><span data-stu-id="c98d1-112">A set of remote procedure calls to a messaging server.</span></span>
    
- <span data-ttu-id="c98d1-113">Все, что можно использовать для передачи данных с одного компьютера на другой.</span><span class="sxs-lookup"><span data-stu-id="c98d1-113">Anything that can be used to transfer data from one computer to another.</span></span>
    
<span data-ttu-id="c98d1-114">DLL поставщика транспорта должен соответствовать интерфейсу, указанному MAPI.</span><span class="sxs-lookup"><span data-stu-id="c98d1-114">A transport provider DLL must conform to the interface specified by MAPI.</span></span> <span data-ttu-id="c98d1-115">Как разработчик поставщика транспорта вы будете реализовывать этот интерфейс с точки зрения функций, присутствующих в системе обмена сообщениями.</span><span class="sxs-lookup"><span data-stu-id="c98d1-115">As a transport provider developer, you will implement this interface in terms of the functionality present in the messaging system.</span></span>
  

