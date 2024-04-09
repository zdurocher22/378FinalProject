from vetiver import VetiverModel
from dotenv import load_dotenv, find_dotenv
import vetiver
import pins

import logging

logging.basicConfig(
    format='%(asctime)s - %(message)s',
    level=logging.INFO
)

load_dotenv(find_dotenv())

b = pins.board_folder('data/model/', allow_pickle_read=True)
v = VetiverModel.from_pin(b, 'penguin_model', version = '20240309T184045Z-a6f9b')

vetiver_api = vetiver.VetiverAPI(v)
api = vetiver_api.app

vetiver_api.run(port = 8080)