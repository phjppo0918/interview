필터는 DispatcherServlet 외부에 존재합니다. 따라서 예외가 발생했을 경우 ErrorController에서 처리해야 합니다.

하지만 인터셉터는 DispatcherServlet 내부에 존재합니다.
따라서 @ControllerAdvice를 적용하여 처리할 수 있습니다.