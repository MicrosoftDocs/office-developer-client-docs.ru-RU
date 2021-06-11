---
title: IMAPIFormMgrResolveMultipleMessageClasses
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIFormMgr.ResolveMultipleMessageClasses
api_type:
- COM
ms.assetid: d3cc6658-e46d-42dd-b1ac-65c88cfef8ca
description: 'Дата последнего изменения: 23 июля 2011 г.'
ms.openlocfilehash: 515061c6c208008c4752e5ff2f23933a4c259c00
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33428020"
---
# <a name="imapiformmgrresolvemultiplemessageclasses"></a>IMAPIFormMgr::ResolveMultipleMessageClasses

  
  
**Область применения**: Outlook 2013 | Outlook 2016 
  
Устраняет группу классов сообщений в их формах в контейнере форм и возвращает массив информационных объектов форм для этих форм.
  
```cpp
HRESULT ResolveMultipleMessageClasses(
  LPSMESSAGECLASSARRAY pMsgClasses,
  ULONG ulFlags,
  LPMAPIFOLDER pFolderFocus,
  LPSMAPIFORMINFOARRAY FAR * ppfrminfoarray
);
```

## <a name="parameters"></a>Parameters

 _pMsgClasses_
  
> [in] Указатель на массив, содержащий имена классов сообщений для решения.
    
 _ulFlags_
  
> [in] Немного флагов, которые контролируют решение классов сообщений. Можно установить следующий флаг:
    
MAPIFORM_EXACTMATCH 
  
> Разрешены только строки класса сообщений, которые соответствуют точному типу.
    
MAPIFORM_LOCALONLY
  
> Не включаем кэшные формы.
    
 _pFolderFocus_
  
> [in] Указатель на папку, содержаную форму, класс сообщений которой решается. Параметр  _pFolderFocus_ может быть NULL. 
    
 _ppfrminfoarray_
  
> [вышел] Указатель на указатель на массив информационных объектов форм. Если зритель формы передает NULL в  _параметре pMsgClasses,_ параметр  _ppfrminfoarray_ содержит информационные объекты формы для всех форм в контейнере. 
    
## <a name="return-value"></a>Возвращаемое значение

S_OK 
  
> ����� ������� � ������ ��������� ��������� ��� ��������.
    
## <a name="remarks"></a>Примечания

Зрители формы называют **метод IMAPIFormMgr::ResolveMultipleMessageClasses,** чтобы разрешить группу классов сообщений для форм в контейнере форм. Массив объектов информации о формах, возвращаемых в  _ppfrminfoarray,_ предоставляет дополнительный доступ к свойствам каждой формы. 
  
## <a name="notes-to-callers"></a>Примечания для вызывающих методов

Чтобы разрешить группу классов сообщений формам, зритель формы проходит в массиве имен классов сообщений, которые необходимо разрешить. Чтобы заставить разрешение быть точным (то есть для предотвращения разрешения для базового класса класса сообщений, когда не доступен точно совпадающий сервер формы), флаг MAPIFORM_EXACTMATCH может быть передан в _параметре ulFlags._ 
  
Имена классов сообщений всегда являются строками ANSI, а не Unicode.
  
Если класс сообщений не удается разрешить в форму, NULL возвращается для этого класса сообщений в массиве сведений о форме. Поэтому, даже если метод возвращает S_OK, зрителям форм не следует работать на предположении, что все классы сообщений успешно решены. Вместо этого зрителям формы следует проверить значения возвращаемого массива.
  
## <a name="see-also"></a>См. также



[IMAPIFormMgr::ResolveMessageClass](imapiformmgr-resolvemessageclass.md)
  
[IMAPIFormMgr : IUnknown](imapiformmgriunknown.md)

