# Urban Flo
1. Keep frontend and backend in same project folder
2. Install nodejs, jdk 17.0.2 x64, sumo win64 1.25.0 and relaunch vscode.
3. Go to frontend>src>simulation-urls.ts 
4. Paste 
export const DOMAIN_NAME = 'localhost:8080';
export const BASE_URL = `http://${DOMAIN_NAME}`;
export const SIMULATION_SOCKET_URL = `ws://${DOMAIN_NAME}/simulation-socket`;
export const BASE_SIMULATION_DATA_TOPIC = '/topic/simulation';
export const BASE_SIMULATION_ERROR_TOPIC = '/topic/simulation/_/error';
export const BASE_SIMULATION_DESTINATION_PATH = '/app/simulation';

5. Go to backend>build.gradle.kts, line 33, set libtraci to 1.25.0
6. First Go to backend Directory in terminal, run .\gradlew.bat clean bootRun
7. Exceuting ~80% means running.
8. Seperate terminal go to frontend directory, run pnpm install, pnpm dev
9. Open Localhost, make triangle road and simulate, wait for red dots to appear.
